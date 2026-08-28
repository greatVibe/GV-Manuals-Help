# Report and follow a support request

Use Support in your profile menu to view your requests, open a request, follow progress, and review linked delivery work without starting another AI turn.

## Before you report

Search your support queue for the same symptom. A repeated report is useful when it adds a new affected node, time, version, or piece of evidence, but avoid creating several records for the same occurrence.

Choose whether the problem belongs to GreatVibe or your own project. Select bug, feature, documentation, performance, security, access, billing, or other. Add severity, the affected platform area or component, what you expected, what happened, and a concise safe reproduction.

For customer-project work, add the repository. When relevant, link the GitHub organization/repository, issue or pull request, and commits. If your organization uses Jira or another connected system, you may also see its linked record.

## Reporter identity

Your signed-in identity is the authoritative reporter and account holder. If Claude, Codex, Mochi, or another agent helps detect or submit the request, its agent, model, and build labels are kept as diagnostic context. Those labels do not replace your authenticated identity unless GreatVibe verifies a signed agent principal.

The original organization, mesh, node, and first-seen time are retained as reporting origin. Later observations can add affected scopes and evidence without rewriting that origin.

## Add safe evidence

Screenshots and files should be point-in-time evidence. Prefer a managed or versioned reference with capture time, media type, and storage version.

Never include:

- passwords, tokens, credentials, or authorization headers;
- raw private prompts or full private logs;
- unnecessary names, email addresses, or personal data;
- mutable or public links that may later show different content;
- another organization's evidence.

Allowed evidence depends on your account policy. GreatVibe validates the reference type, capture time, media type, and version before accepting it.

## Understand the request lifecycle

The shipped lifecycle states are new, triaged, acknowledged, resolved, and dismissed. Later SDLC rollout phases add in progress, waiting for customer, waiting internally, closed, and explicit duplicate outcomes. Konui shows only transitions currently enabled for your account.

Severity describes impact. Priority describes delivery order. They can differ. An SLA panel may show acknowledgement and resolution targets, pauses, and breach risk according to your support plan.

Use a public reply to add customer-visible information. Internal support notes and employee-only assignment details are not shown unless your role allows them.

## Follow agile delivery

When planning is enabled, a request can link to native delivery work:

- Initiative for a strategic outcome;
- Epic for a large outcome;
- Feature for a customer capability;
- Story for user-visible behavior;
- Bug for incorrect behavior;
- Task for implementation work.

Linked work may appear in a backlog, Sprint, and Release. The request detail can show acceptance criteria, owner/team, blockers, commits, pull requests, checks, builds, deployments, and verification. The support lifecycle remains separate, so a pull request being merged does not automatically mean your request is resolved.

## GitHub and Jira links

GreatVibe remains the native support record. GitHub or Jira links are synchronized projections when your administrator enables them.

The integration may create or link an issue, apply mapped labels and status, place work in a milestone or iteration, and show branches, commits, pull requests, checks, releases, and deployments. If both sides change the same managed field, you may see a sync conflict while an authorized operator chooses the correct value.

Provider outages do not remove your native request. A disconnected integration stops syncing but leaves the GreatVibe history intact.

## Repeated reports and privacy

Privacy-safe fingerprints can connect repeated symptoms. Support staff may see that a pattern affects several organizations, meshes, or nodes, while customers do not see other reporters' identities or data.

The detail view separates GreatVibe remediation from customer-project work. It shows only the evidence, conversation, lifecycle, planning, integration, and assignment information your role is allowed to see.

## Notifications

Watch a request to receive updates. Notifications use your verified account channels when enabled. Do not put an email address or phone number in the ticket body.

Important notifications can include acknowledgement, a request for information, SLA risk, resolution, reopen, linked release, deployment, or connector conflict.

## Common actions

### Add a new observation

Open the existing request, add the affected node/version/time and safe new evidence, then submit. The occurrence count and affected scopes may update while original attribution and classification stay unchanged.

### Answer a support question

Reply in the public conversation and attach only the requested safe evidence. A waiting-customer request can return to active processing after your response.

### Verify a fix

Review the resolution summary and linked release/deployment, repeat the safe reproduction, and record pass or fail. A failed verification may reopen the request.

### Report a security issue

Choose security and the correct severity, provide the minimum safe detail, and avoid exploit secrets or credentials. Follow any private security-reporting route shown by your account.

## If something looks wrong

- Wrong reporter: confirm you are signed into the correct account; agent labels are only diagnostics.
- Missing request: check organization, filters, node, and lifecycle state.
- Rejected attachment: check approved scheme, capture timestamp, version, media type, size, and privacy policy.
- GitHub/Jira not updating: check the sync status and contact your organization support administrator.
- Wrong owner or private note visible: stop sharing the view and report a security issue immediately.
