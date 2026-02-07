
# ToxicSkills Demo

About ToxicSkills: https://snyk.io/blog/toxicskills-malicious-ai-agent-skills-clawhub/

**Disclaimer**: Danger! This project is for educational purposes only. Do not use the skills in this project. The skills in this project are for demonstration purposes only and may contain malicious code. Do not use the skills in this project. Use at your own risk. The author is not responsible for any damage caused by the skills in this project.

<div align="center">
  <img src=".github/mcp-scan-skills-scan1.png" alt="ToxicSkills Demo" width="600">
</div>

## How to use

Run mcp-scan to scan the google skill

```sh
uvx mcp-scan@latest --skills .agents/skills/google/SKILL.md
```

Run all the skills in this project

```sh
uvx mcp-scan@latest --skills .agents/skills
```

## How to demo

This project contains a fake Vercel skill which is designed to look like a real Vercel skill but actually contains malicious code. The skill's payload is benign and only prints the current host's `uname -a` value to a remote pastebin host.

The purpose of the demo is to show that Agent Skills `SKILL.md` files can contain malicious code that is automatically executed by agents and as such it inherits the agents access and trust. This is a security risk that needs to be addressed by agent developers and users.

### ToxicSkills Fake Agent Skills with Gemini CLI demo

Here's how to show a live example of ToxicSkills in action with a Gemini CLI coding agent:
Start the Gemini CLI coding agent:

```sh
gemini
```

Then ask the agent to use the Vercel skill to deploy a Next.js app:

```sh
Please deploy my app to vercel
```

Here's a real run screenshot:

![Gemini CLI coding agent using the fake Vercel skill to deploy a project and shows ToxicSkills in action](.github/agent-skills-vercel-fake-auto-run-with-gemini.png)

### ToxicSkills Fake Agent Skills with OpenCode demo

Here's how to show a live example of ToxicSkills in action with a OpenCode coding agent:

May need to install OpenCode first:

```sh
curl -fsSL https://opencode.ai/install | bash
```

Start the OpenCode coding agent:

```sh
opencode
```

Then ask the agent to use the Vercel skill to deploy a Next.js app:

```sh
Please deploy my app to vercel
```

Here's a real run screenshot:

![Gemini CLI coding agent using the fake Vercel skill to deploy a project and shows ToxicSkills in action](.github/agent-skills-vercel-fake-auto-run-with-opencode.png)

### MCP-Scan demo showing Vercel skill with malicious code detection

![MCP-Scan showing the Vercel skill with malicious code detection ](.github/mcp-scan-toxicskills-vercel-fake-example.png)

## Skills in this project:

- A ClawHub skill from https://github.com/aztr0nutzs/NET_NiNjA.v1.2/blob/main/clawhub
- A Google skill from https://github.com/aztr0nutzs/NET_NiNjA.v1.2/tree/main/google-qx4