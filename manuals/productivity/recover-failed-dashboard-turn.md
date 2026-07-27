# Recover a Failed Dashboard Turn

When a dashboard turn ends unexpectedly, the work may not appear as a normal gvturn card. Use recovery to capture what is known, preserve the request id, and decide whether the original task should be retried.

## When to use this

Use this manual when the console shows a failed or missing turn, when a request id is available but no result card appears, or when a workflow needs an audit trail before continuing.

## What you need

Keep the request id, the dashboard session, and any visible error title. A title such as `Turn Failed: Turn ended unexpectedly` is enough to start a recovery card, but it may not contain the original work product.

## Recovery steps

1. Create a recovery gvturn for the missing or failed request.
2. Record the original request id exactly as shown in the console.
3. Check whether a raw turn, metadata record, graph edge, or prior gvturn exists for that id.
4. If a record exists, summarize the recovered result and link the relevant ids.
5. If no record exists, say that the request appears to have failed before durable capture.
6. Choose whether to retry the original prompt or inspect lower-level logs.

## What recovery can and cannot do

Recovery can preserve the known failure state, request id, session id, timestamps, and lookup results. It cannot reconstruct model output that was never persisted, and it should not mark unrelated pending items complete unless the failed request is confidently matched to them.

## Recommended wording

Use direct status language:

`The request id was inspected, but no persisted raw-turn record was found. Retry the original request if the missing work product is still needed.`
