# What Is A Connector?

A connector is a saved link from your node to an outside service.

It names the service, points to it, and says which credential to use. It also
knows how to check that the service is up. Your agent reads the connector, so
it can use the service the right way without you repeating the details.

## What A Connector Holds

| Part | What it means |
| --- | --- |
| Name and ID | A short label you and your agent use, such as `builds-prod` or `assets-bucket`. |
| Target | Where the service lives: a web address, a host, or a command-line tool. |
| Credential | A reference to a credential you saved. The connector never holds the secret itself. |
| Health check | A safe test the node runs to see if the service answers. |
| Settings | Extra details, such as a region, a bucket name, or which platform it is. No secrets go here. |
| Usage notes | Hints that tell your agent which tool to use and what a good first call looks like. |
| Proxy rules | Optional. For web APIs, the node can make calls for the agent, add the credential, and only allow the paths and methods you expect. |

## Where Connectors Live

A connector belongs to one node. It is not copied to other nodes. If you work
on two nodes and need the same service on both, add the connector on each one.

## Status

Each connector shows a status after its health check:

- **Healthy**: the service answered.
- **Degraded**: the service answered with a problem.
- **Offline**: the service did not answer, or the check failed.
- **Unknown**: no check has run yet.

## Templates

Most connectors start from a built-in template. A template fills in the
target, the health check, the usage notes and safe proxy rules for a common
service. You add a name, pick the credential, and fill in any settings the
service needs.

See `../reference/connector-template-types.md` for the full list.

## Categories

Connectors are grouped by kind. Common groups are AI services, cloud accounts,
databases, caches, queues, web APIs, storage, CI/CD and object storage.

- **CI/CD** connectors let your agent read the latest build and pipeline state.
- **Object storage** connectors let your agent list and move files in buckets
  and containers.

## Safety

- Keep the secret in a credential. Never in connector settings, names or notes.
- Give the credential the least access that still does the job.
- Web API connectors only allow the paths and methods their rules list.
- Checks are read-only.

## Related Guides

- `../how-to/connect-cicd-and-cloud-storage.md`
- `../how-to/builtin-credential-and-connector-templates.md`
- `../reference/connector-template-types.md`
- `what-is-a-node.md`
