# DevOps: CI/CD, Cloud And Infrastructure As Code

greatVibe doesn't replace your pipeline. It connects to it, reads its state as
evidence, and helps you change infrastructure through gated, reviewable steps.

## Connect Your Pipeline

Save a credential, then add a CI/CD connector from a template. Step by step:
`../../how-to/connect-cicd-and-cloud-storage.md`. Templates:
`../../reference/connector-template-types.md`.

| Template | Platform | How state is read |
| --- | --- | --- |
| AWS CodePipeline | `aws-codepipeline` | Pipeline state through the AWS tools |
| GitHub Actions | `github-actions` | Recent workflow runs for a repository |
| GitLab CI | `gitlab-ci` | Recent project pipelines |
| Azure DevOps | `azure-devops` | Pipeline runs |
| Google Cloud Build | `google-cloud-build` | Recent builds |
| Jenkins | `jenkins` | Last build of a job |
| Self-hosted | `self-hosted` | A status URL you provide, read-only (Buildkite, TeamCity, Drone, Argo, Tekton and similar) |

A connector counts as a CI/CD source when its category is CI/CD or it carries
a CI/CD platform tag. Agents list sources with `connector_cicd_list`, which
returns each source's platform and the right tool to query it.

## Read Pipeline State

**Procedure:**

1. "List my CI/CD sources."
2. "What is the state of the `my-service` pipeline?" For CodePipeline the agent
   reads the pipeline state with the connector; for HTTP platforms it calls
   the connector's latest-state request through the connector proxy.
3. Open the CI/CD space in Agent IQ.

The CI/CD space reports by exception: pipelines in flight, pipelines acted on
in this turn, and pipelines whose status changed. Unchanged runs sit behind
**Show all**. Progress is counted only from finished stages over a known total;
stages that weren't reported stay unknown and are never invented.

### Peripheral Vision

For AWS CodePipeline sources, greatVibe also samples every pipeline in the
background about once a minute. Failed or stopped pipelines appear in the CI/CD
space even if nobody touched them this turn, and up to five of them are passed
to each new turn as alerts. Agents mention them when they relate to the work.

## Read The Cloud

AWS tools are split by risk:

| Tool | Allowed |
| --- | --- |
| Typed read tools | Identity, EC2, S3, IAM, ECS, load balancers, Lambda, API Gateway, CloudFormation, CodePipeline, CodeBuild, CloudFront, Route 53, Organizations, cost and forecast |
| `aws_cli_read` | Any AWS command whose name starts `describe-`, `list-`, `get-`, `batch-get-`, `head-`, `lookup-`, `simulate-`, or is `scan`/`query` |
| `aws_cli_apply` | Any other AWS command. Write-gated |
| `aws_cloudformation_deploy`, `aws_cloudformation_delete_stack` | Stack changes. Write-gated |

Start every AWS session with an identity check ("which AWS account am I
in?"), then name the profile and region on each request.

## Change The Cloud Safely

Every write tool is **confirmation-gated**. The first call returns a prompt
describing the change and does nothing. It runs only when called again with
`confirmed: true`, which the agent does after you approve.

Running a write across many accounts at once (organization fan-out) needs a
second, explicit opt-in. Without it the tool refuses.

**Procedure: a CloudFormation change.**

1. "Validate `infra/my-service.yaml` and create a change set for stack
   `my-service-dev`. Don't execute it."
2. Read the change set in the card and the IaC space: added, modified and
   removed resources.
3. "Execute the change set." The agent shows the confirmation prompt; approve.
4. Watch stack events in the IaC space until the stack reaches a final status.

## Infrastructure As Code

The IaC space recognises and summarises:

| Tool | Commands |
| --- | --- |
| Terraform, OpenTofu, Terragrunt | plan, apply, destroy |
| AWS CloudFormation | change sets, deploy, stack events |
| AWS SAM | deploy, sync, delete |
| AWS CDK | diff, synth, deploy, destroy |
| Pulumi | preview, up, destroy, refresh |
| Azure | deployments and Bicep |

Resource change counts come only from parsed plan or change-set output.

### A Gated Plan/Apply Pattern That Works

1. One build specification runs in **plan** or **apply** mode.
2. Plan mode: pin the tool version by checksum, run format, init and validate,
   then save the plan to a file. Retry only on known transient errors.
3. A manual approval step reviews the saved plan.
4. Apply mode consumes that exact saved plan file, never a fresh plan.
5. A final gate fails the run if anything is out of place.

Pin pipelines to a reviewed source revision when you need a strict release,
or let them run on push for continuous delivery.

## Delivery Evidence In Agent IQ

| Space | Shows | Truth rule |
| --- | --- | --- |
| Builds | Go, Deno, TypeScript, make, npm, cargo, docker, gradle, Xcode, CodeBuild | Passed or failed only from a real result |
| Tests | Recognised test and check runs, plus your declared test plan | Counts only from finished runs |
| CI/CD | Pipeline runs and stage graph across providers | Progress only from finished stages |
| IaC | Plans, change sets and stack events | Change counts only from parsed output |
| Sleeping | Background waits and long processes | Done only on a terminal signal |

## Procedure: Release A Service

1. Turn ends with commit; audit if `audit_required`.
2. "Push `my-service`." Or "Merge into the release branch and push."
3. "Watch the `my-service` pipeline until it finishes." The agent tracks the
   wait and refreshes the CI/CD space.
4. If a stage fails: "Show the failed stage's logs and fix the cause." The fix
   is a new turn, commit and push.
5. After deploy: "Run the post-deploy smoke tests." These fill the
   `post-deploy` rows of the test plan.

## Related

- `nodes-builds-and-tests.md`
- `git-and-repositories.md`
- `security-and-secrets.md`
- `../../concepts/what-is-a-connector.md`
- `../../how-to/add-aws-credential.md`
