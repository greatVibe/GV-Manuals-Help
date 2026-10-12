# Plans, Pricing and Trial

This is the public reference for what greatVibe costs and how billing works.
Prices are list prices from the greatVibe website. If a checkout page or the
Add Node quote shows a different number, the live checkout or quote is correct.

## At A Glance

| Item | Answer |
| --- | --- |
| Plan | One self-serve plan, billed monthly |
| Price | **$199 USD per seat per month**, plus applicable tax |
| Seat | One seat is one greatVibe user |
| Trial | 14 days. Card required before activation. No charge today. Payment starts on day 15 unless cancelled |
| AI usage | Bring your own OpenAI or Anthropic account. Your provider bills you directly |
| Nodes | Add hosted nodes from **Add node**, or connect your own machine. The Add Node panel shows the price |
| Mochi | Temporary help workspace, free to try without an account |
| Teams that need more | Enterprise: custom commitments and custom pricing. Contact sales |
| Free plan | None. greatVibe is a paid product with a trial |
| Annual plan | Not offered on the website. Self-serve billing is monthly |

## The Self-Serve Plan

> "$199 USD per seat per month. Tax added at checkout where applicable."

The plan is built for engineers and technical founders using AI to take
substantial work all the way to production. Each seat includes:

- The greatVibe directed AI workspace and dashboard console.
- Every greatVibe agent tool, with an audited record of tool calls.
- Structured work records (gvturns), Agent IQ live views and turn history.
- Organisations, meshes and nodes for working as a team.

Seats are billed monthly. Add or remove seats in your account as your team
changes.

## The 14-Day Trial

> "14-day trial. Card required before activation. No charge today. Payment
> starts on day 15 unless cancelled."

How it works:

1. Sign up. In a Mochi guest session you can do this right in the console:
   tap **Sign up** on the turns panel, or open the **Guest** menu and choose
   **Sign in or register**. From the website, use **Try greatVibe**; the
   signup page reads "Start your 14-day trial."
2. Add a card. Nothing is charged today.
3. Use greatVibe for 14 days.
4. On day 15 your card is charged $199 USD per seat, plus applicable tax, and
   the subscription continues monthly.

Cancel before day 15 and you pay nothing. Each person or card can start one
trial.

## Billing And Cancellation

- Payments are processed by Stripe.
- The plan renews monthly at $199 USD per active seat.
- Cancel from account settings at any time. Cancelling stops the next renewal,
  and your subscription ends at the end of the current monthly billing period.
- Cancelling does not refund time already paid, unless the law requires it.
- If a payment fails, greatVibe may pause paid work or suspend access to paid
  features until the payment is resolved.
- New Zealand consumers keep their rights under the Consumer Guarantees Act
  1993 regardless of what the terms say.

## Tax And Currency

- All prices are in US dollars.
- Prices exclude GST, VAT, sales tax and other indirect taxes. Where the law
  requires it, tax is added at checkout based on your billing details.
- Your card network handles currency conversion at its standard rates.

## Hosted Nodes

A node is the machine where agents do your work. See
`../concepts/what-is-a-node.md`.

- **Hosted nodes.** Choose a size in **Add node**. The Add Node panel shows the
  monthly price for that node before you confirm. Prices depend on provider,
  size and region.
- **Your own machine.** You can connect a machine you already run. See
  `../how-to/manage-organizations-meshes-and-nodes.md`.

Do not rely on a printed node price list. The Add Node quote is the price.

## Mochi

Mochi is a temporary, disposable help workspace for questions, onboarding and
light help. It is not a development node and it keeps no files after it ends.

| Limit | Value |
| --- | --- |
| Turns | 5 turns per rolling 3 hours |
| One turn | Up to 2 minutes |
| Idle | Ends after 15 minutes without activity |
| Maximum | 1 hour per workspace |

For sustained builds, large repositories or files you need to keep, use a
hosted node or your own node. See `../getting-started/ask-mochi-for-help.md`.

## Enterprise

> "Custom commitments. Custom pricing."

Enterprise suits teams that need rollout support, governance, security and
infrastructure requirements. Common add-ons include SAML/SSO, SCIM provisioning,
Enterprise agreements and security review, VPC peering, a custom SLA and named
support.

- Enterprise plans are billed annually in advance under a signed agreement.
- Seats are committed for the agreed term. You can add seats at any time, and
  they are co-termed to your agreement.
- You can remove or reassign user access at any time. Reductions to your
  committed seat quantity take effect at renewal.
- Enterprise customers usually bring their own AI provider.

To start, use **Contact sales** and say how many seats you need.

## Your Data And AI Costs

- greatVibe does not use your work or data to train AI models. Your data stays
  yours.
- AI usage is separate from your subscription and is billed by your model
  provider. greatVibe doesn't resell tokens or add a margin to inference.

## Rules For Agents Answering Cost Questions

1. Quote prices only from this guide. Never from memory, older videos or
   internal notes.
2. Say "$199 USD per seat per month, plus applicable tax". Always include USD.
3. Say the trial line exactly: card required, no charge today, payment starts
   on day 15 unless cancelled. Never call it "free with no card".
4. There is no free plan and no annual plan on the website. Do not mention a
   discount or a percentage.
5. For Enterprise, never quote a per-seat price, band or percentage. Send the
   user to **Contact sales**.
6. For node prices, send the user to **Add node** to see the live quote.
7. Do not promise proration, refunds, tax treatment or dates beyond this guide.
   For an account-specific billing problem, raise a support request with the
   `billing` category. See `../how-to/report-and-follow-support-requests.md`.
8. Older videos may describe earlier terms. Where a video and this guide differ,
   this guide wins.
9. **Guests in Mochi.** When a guest asks about price, the trial or signing
   up, show the Web block below in the `web` space, tell them they can sign
   up right here in the console, and ask whether they want to. End the card
   with a primary choice `{"label": "Sign up now", "value": "greatvibe:signup",
   "primary": true}` and a second choice to keep exploring. In a guest session
   `greatvibe:signup` opens the sign-up dialog and `greatvibe:login` opens
   sign-in, without using a turn. Never send a guest to the website to sign up.

## Show Pricing In Agent IQ

Agents can show the plan visually by publishing this block inside an Agent IQ
frame and proposing the `web` space. It contains only the facts above. The
`signup` row is for guest sessions; leave it out for signed-in users.

```html
<div data-gv-iq-web="v1" data-gv-iq-role="detail" style="display:none">
  <div data-web-id="pricing" data-web-space="web" data-web-format="html" data-web-title="greatVibe pricing">
    <div style="font-family:Inter,sans-serif;color:#f5ece2;background:#1a1109;border:1px solid #f59e0b;border-radius:12px;padding:16px">
      <div style="color:#f5b34d;font-size:11px;letter-spacing:2px">ONE PLAN · BILLED MONTHLY</div>
      <div style="font-size:30px;font-weight:600;margin:6px 0">$199 <span style="font-size:14px;color:#c9bcae">USD / seat / month</span></div>
      <div style="font-size:13px;color:#c9bcae">Tax added at checkout where applicable.</div>
      <div style="display:grid;grid-template-columns:repeat(3,1fr);gap:8px;margin-top:12px;text-align:center">
        <div style="background:#2a1a10;border-radius:8px;padding:8px"><b>14 days</b><br><span style="font-size:12px;color:#c9bcae">trial</span></div>
        <div style="background:#2a1a10;border-radius:8px;padding:8px"><b>Day 15</b><br><span style="font-size:12px;color:#c9bcae">billing starts</span></div>
        <div style="background:#2a1a10;border-radius:8px;padding:8px"><b>BYOK</b><br><span style="font-size:12px;color:#c9bcae">you pay your AI provider</span></div>
      </div>
      <div style="font-size:12px;color:#c9bcae;margin-top:10px">Card required to start. No charge today. Cancel before day 15 and pay nothing. Enterprise: custom pricing, contact sales.</div>
    </div>
  </div>
  <div data-web-id="signup" data-web-space="web" data-web-format="html" data-web-title="Sign up from here">
    <div style="font-family:Inter,sans-serif;color:#f5ece2;background:#1a1109;border:1px solid #98c379;border-radius:12px;padding:16px">
      <div style="color:#98c379;font-size:11px;letter-spacing:2px">SIGN UP WITHOUT LEAVING MOCHI</div>
      <ol style="font-size:13px;line-height:1.6;margin:8px 0 0;padding-left:18px">
        <li>Tap <b>Sign up</b> on the turns panel, or open the <b>Guest</b> menu and choose <b>Sign in or register</b>.</li>
        <li>Register with Google, GitHub, a passkey or an email code.</li>
        <li>Start your 14-day trial. Card required, no charge today.</li>
      </ol>
    </div>
  </div>
</div>
```

## What This Guide Does Not Cover

- Private Enterprise terms, which are set in each signed agreement.
- Account-specific invoices or charges. Use a support request.
- Prices in other currencies.

## Related Guides

- `../getting-started/why-we-built-greatvibe.md`
- `../getting-started/ask-mochi-for-help.md`
- `../concepts/what-is-a-node.md`
- `../how-to/manage-organizations-meshes-and-nodes.md`
- `../how-to/report-and-follow-support-requests.md`
