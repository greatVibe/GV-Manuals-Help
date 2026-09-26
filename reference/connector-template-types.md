# Connector Template Types

Built-in templates you can start a connector from. Each one sets the target,
the health check and the usage notes. You add the name, the credential and any
settings listed.

To see the live list on your node, ask: **"List the connector templates."**

## CI/CD

Read the latest build, pipeline, run and stage state.

| Template | Service | Credential | Health check | Settings |
| --- | --- | --- | --- | --- |
| `cicd-aws-codepipeline` | AWS CodePipeline | AWS | Lists one pipeline | `region`; optional AWS account pin |
| `cicd-github-actions` | GitHub Actions | API key (token) | Reads the token's user | None |
| `cicd-gitlab` | GitLab CI/CD | API key (token) | Reads the token's user | Self-managed: your GitLab address |
| `cicd-azure-devops` | Azure DevOps Pipelines | Basic auth (`:TOKEN`) | Reads your profile | None |
| `cicd-google-cloud-build` | Google Cloud Build | Google Cloud key | Lists one build | None |
| `cicd-jenkins` | Jenkins | Basic auth (`user:apiToken`) | Reads the Jenkins API | Your Jenkins address |
| `cicd-self-hosted` | Other CI/CD with a web status API | API key | Calls your address | Your address and status path |

Each CI/CD connector records its platform and the call that returns the
latest state, so your agent can go straight to it.

## Object Storage

List, read and write files in buckets and containers.

| Template | Service | Credential | Health check | Settings |
| --- | --- | --- | --- | --- |
| `objstore-aws-s3` | Amazon S3 | AWS | Checks the bucket, or lists buckets | Optional `bucket`, `region`, AWS account pin |
| `objstore-azure-blob` | Azure Blob Storage | Connection string (account key or SAS) | Checks the container, or lists containers | Optional `container`, `account` |
| `objstore-gcs` | Google Cloud Storage | Google Cloud key | Checks the bucket, or lists buckets | Optional `bucket` |
| `objstore-s3-compatible` | Cloudflare R2, Vultr Object Storage, Wasabi, MinIO, Backblaze B2 and other S3-style stores | AWS-style key saved as JSON | Checks the bucket, or lists buckets, at your endpoint | Required `endpoint`; optional `region` (R2 uses `auto`), `bucket` |

Older `aws-s3` and `minio` templates still work for connectors that use them.
For new connectors, use the `objstore-` templates.

## AI Services

| Template | Service | Credential |
| --- | --- | --- |
| `anthropic` | Anthropic API | API key |
| `openai` | OpenAI API | API key |

## Cloud Accounts

| Template | Service | Credential |
| --- | --- | --- |
| `aws-cli` | AWS account | AWS |
| `gcp-cli` | Google Cloud project | Google Cloud key |
| `vultr` | Vultr API | API key |
| `binarylane` | Binary Lane API | API key |
| `ec2-ssh` | SSH to an AWS EC2 instance | SSH key |

## Databases, Caches And Queues

| Template | Service | Credential |
| --- | --- | --- |
| `postgres` | PostgreSQL | Connection string |
| `mysql` | MySQL | Connection string |
| `mongodb` | MongoDB | Connection string |
| `aws-aurora` | AWS Aurora | AWS |
| `aws-aurora-dsql` | AWS Aurora DSQL | AWS |
| `elasticsearch` | Elasticsearch | Basic auth |
| `redis` | Redis | Connection string |
| `kafka` | Apache Kafka | Connection string |
| `rabbitmq` | RabbitMQ | Basic auth |

## Web APIs

| Template | Service | Credential |
| --- | --- | --- |
| `github` | GitHub API | API key (token) |
| `cloudflare` | Cloudflare API | API key |
| `slack` | Slack Web API | API key |
| `stripe` | Stripe API | Basic auth |
| `http-api` | Any web API | API key |
| `greatvibe-mesh` | Another greatVibe mesh you are allowed to reach | Bearer token |

## Other

| Template | Service | Credential |
| --- | --- | --- |
| `ssh` | Any SSH server | SSH key |
| `github-ssh` | GitHub over SSH (clone and push) | SSH key |
| `docker-registry` | Container image registry | Basic auth |
| `aws-s3` | Amazon S3 (older template) | AWS |
| `minio` | MinIO (older template) | AWS-style key |

## Related Guides

- `../concepts/what-is-a-connector.md`
- `../how-to/connect-cicd-and-cloud-storage.md`
- `../how-to/builtin-credential-and-connector-templates.md`
