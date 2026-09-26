# Connect CI/CD And Cloud Storage

Add a connector so your agent can read build state or work with files in a
bucket. You need a saved credential first, then one connector that uses it.

## Before You Start

1. Pick the template for your service. See `../reference/connector-template-types.md`.
2. Create a credential with the least access that does the job. For AWS, see
   `add-aws-credential.md`. Enter secrets only in the secure credential form or
   with Sealed Secret. Never paste them into a prompt.
3. Note any settings the template needs, such as a region or a bucket name.

## Step 1: Save The Credential

Ask: **"Open the Add Credential wizard."** Pick the matching credential type:

| Service | Credential type | Good scope |
| --- | --- | --- |
| AWS CodePipeline or Amazon S3 | AWS | Read-only pipeline access, or access to one bucket |
| GitHub Actions | API key (token) | Fine-grained token with Actions read |
| GitLab CI/CD | API key (token) | Token with read API |
| Azure DevOps | Basic auth | Personal access token with Build read. Store it as `:TOKEN` (empty user name) |
| Google Cloud Build or Cloud Storage | Google Cloud | Service account key with a viewer role |
| Jenkins | Basic auth | `user:apiToken` |
| Azure Blob Storage | Connection string | A storage connection string. Use a SAS form when you can |
| S3-compatible storage | AWS | Access key saved as JSON: `{"accessKeyId":"…","secretAccessKey":"…"}` |

## Step 2: Add The Connector

Ask your agent in plain words. Name the template, the credential and the
settings. For example:

- "Add a connector called `builds-prod` from the `cicd-github-actions`
  template, using my GitHub Actions token."
- "Add a connector called `pipelines` from the `cicd-aws-codepipeline`
  template, using my AWS credential. Set region to `us-east-1`."
- "Add a connector called `assets` from the `objstore-s3-compatible` template,
  using my storage key. Set endpoint to `https://storage.example.com`, region
  to `auto` and bucket to `assets`."

The agent uses the connector tools (`connector_templates`,
`connector_register`). To see your connectors on screen, ask: **"Open the
connectors card in Settings."**

## Step 3: Check It

Ask: **"Check the health of `builds-prod`."** A healthy result means the
service answered with your credential.

If the check fails:

- **Offline**: check the address, the credential, and that the node can reach
  the service.
- **Degraded**: the service answered with an error. Check the token scope.
- **Setting error**: a bucket or endpoint value is not valid. Fix the setting.

## Step 4: Use It

For CI/CD:

- "What is the latest run on `builds-prod`?"
- "Which pipelines failed today?"

Ask your agent to list your CI/CD sources first. The **CI/CD** space in Agent
IQ shows those sources and the runs your agent checked this turn. It shows
what is in flight, what changed, and what the agent acted on.

For storage:

- "List the first 20 files in the `assets` bucket."
- "Upload `report.pdf` to `assets/reports/`."

## Tips

- **One CI/CD source per account.** Add one CI/CD connector for each account
  or organisation. Two connectors for the same account show the same
  pipelines twice.
- **Set a bucket for tight keys.** Some keys can use one bucket but cannot
  list all buckets. Set the bucket so the health check tests that bucket.
- **Updating settings replaces them.** When you change a connector's settings,
  send every setting you want to keep, not only the new one. A setting you
  leave out is removed.
- **Pin the AWS account.** For AWS connectors, you can set the expected
  12-digit account number. The node checks it before every call and stops if
  the credential points at a different account. Do not set it on
  S3-compatible storage.
- **Keep secrets out of settings.** Settings, names and notes are visible.
  Secrets belong in the credential only.

## Related Guides

- `../concepts/what-is-a-connector.md`
- `../reference/connector-template-types.md`
- `builtin-credential-and-connector-templates.md`
- `add-aws-credential.md`
- `add-github-credential.md`
