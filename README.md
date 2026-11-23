<div align="center">
  <img src=".agents/skills/linkedin-networking/assets/networking-256.png" width="112" height="112" alt="">
  <h1>LinkedIn Networking</h1>
  <p>A Codex skill for finding people worth connecting with and choosing posts to engage with.</p>
</div>

## Start a session

1. Clone this repository or download and extract it. Open the repository folder as a local project in a current version of Codex, trust it if prompted, and start a chat in that project.
2. Each person runs the skill in their own Codex session and signs in to their own LinkedIn account. Ask for a Dot handoff if you want to work with LinkedIn open beside the chat.
3. Invoke `$linkedin-networking` and give it a goal. For a review, share the relevant profile links, brief post summaries, or connection status you see.

```text
Use $linkedin-networking to prepare my next LinkedIn session. Open Dot if
available. Help me pick people to connect with and posts from my followers
to react to based on the profiles and posts I share.
```

| Ask for | What you get |
| --- | --- |
| Connection suggestions | A shortlist with reasons, known invitation status, and optional notes. |
| A follower post review | Posts worth your attention and a suggested reaction for each relevant post. |
| A comment, reply, or follow-up | A draft you can review in context. |
| A specific reaction or invitation | A verified result with the appropriate LinkedIn-authorized integration, or the target and next step for you in the browser. |

## Browser and account access

Dot is the preferred browser when Computer Use lists it. In the manual flow, you browse LinkedIn and click Like, Connect, or Send yourself. Direct actions require an authorized LinkedIn integration with the relevant account and permissions. The skill works with the material you share when live access is unavailable. [Account access and browser handoff](.agents/skills/linkedin-networking/references/access.md) · [LinkedIn's automation rules](https://www.linkedin.com/help/linkedin/answer/a1341387)

## Model settings

The trusted project defaults to **GPT-6.2 Sol** at **xhigh**. In a client that uses a model picker, select those values when starting a chat if your session has a different selection. [Project model settings](.codex/config.toml) · [Codex configuration](https://learn.chatgpt.com/docs/config-file/config-basic)

For an explicit model and reasoning override in the Codex CLI, run this from the repository folder.

```sh
codex -m gpt-6.2-sol -c model_reasoning_effort=xhigh
```

[Skill instructions](.agents/skills/linkedin-networking/SKILL.md)
