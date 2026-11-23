# Account access and browser handoff

## Identify the account owner

Use one account per run. In an authorized integration, verify the authenticated member matches the intended owner before reading account data or sending a change. Use the member's display name or profile URL to resolve ambiguity. The owner completes sign-in and any verification in the official LinkedIn interface. Keep credentials, verification codes, cookies, and access tokens out of chat and project files.

LinkedIn requires members to keep their personal accounts separate and prohibits unauthorized browser automation for actions such as adding contacts and liking posts. Use a LinkedIn-authorized connector for supported reads and writes. Use the manual handoff for the rest. [LinkedIn User Agreement](https://www.linkedin.com/legal/user-agreement) · [Prohibited software and extensions](https://www.linkedin.com/help/linkedin/answer/a1341387)

## Prepare Dot for the owner

1. For a requested browser session or a live task that needs the manual path, use the Computer Use browser tools. Follow the tool's initialization instructions and check the browser inventory for `dot`.
2. When Dot is listed and the owner needs a tab, open a visible blank one with `cua.createBrowserTab("dot", undefined, { visible: true })`. Use the documented handoff control when available and give the owner the sign-in link to open themselves. If they already have their LinkedIn tab open, have them switch to it. [LinkedIn sign-in](https://www.linkedin.com/login)
3. If Dot is absent, say so and continue in a browser the owner selects or with material they share in chat. Leave sign-in, browsing the signed-in site, and any LinkedIn clicks to the owner in the manual path.
4. Ask the owner for only the shortlist inputs needed for the request, such as profile links, brief post summaries, or the invitation or reaction status they see. Prepare the review or draft from those inputs. For a manual action, give the exact target and suggested step and let the owner confirm what they did.

## Use an authorized LinkedIn integration when connected

Check the available connector for the specific read or write, the member identity, and the granted permission. The account owner authorizes the connector through LinkedIn's sign-in and consent flow. A basic identity grant establishes the account. Feed reads, reactions, and invitations each depend on the app's entitled endpoints and scopes. Invitation API access is restricted to approved partners. [LinkedIn API access](https://learn.microsoft.com/en-us/linkedin/shared/authentication/getting-access) · [Reactions API](https://learn.microsoft.com/en-us/linkedin/marketing/community-management/shares/reactions-api) · [Invitations API](https://learn.microsoft.com/en-us/linkedin/shared/integrations/communications/invitations)

- Before sending a write, resolve the exact target and action authorized by the owner. A request to review posts or suggest people calls for a shortlist. For selected targets, check existing state when the integration exposes it, and skip an already applied reaction or pending invitation.
- Use the supported success response or a status read to verify the result. If a write times out or its outcome is unclear, check the state before retrying. If the state cannot be determined, report it as unverified and let the owner verify in LinkedIn.
- When the required connector, capability, permission, or target is unavailable, prepare the manual action using the information on hand. Use the owner handoff if LinkedIn presents a sign-in prompt, verification challenge, or restriction.
