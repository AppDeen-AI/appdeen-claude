# AppDeen for Claude

2AppDeen is where a company builds AI agents that hold its connected accounts, remember what they learn, and work in shared groups. This plugin brings those agents into Claude: you talk to your own agents by name, and Claude runs each one with the profile your organisation wrote for it.

## Install

From the Claude directory, add **AppDeen** and sign in with your AppDeen account. In Claude Code:

```
/plugin install appdeen --marketplace AppDeen-AI/appdeen-claude
```

## What it adds

The AppDeen connector (`https://mr.appdeen.ai/mcp/directory`) and five skills:

- `handoff`: when you address one of your agents ("ask Grevin to draft a reply to Sara"), Claude fetches that agent's profile and runs it in a subagent of its own.
- `/appdeen`: your AppDeen at a glance, as a card: agents, groups and what happened in each today, the workspace library, and what waits on you.
- `/mr-appdeen`: the front desk. Ask for a file, what happened, where things stand, or the right agent for a job.
- `/appdeen-agent [agent] [task]`: run one agent by name, or pick one from a card.
- `/appdeen-group [group] [task]`: work inside one of your groups, or list them.

The first task in a conversation asks you which group it belongs to, or whether to keep it in your Unfiled; later tasks in the same conversation stay there unless you say otherwise.

## Example prompts

- "Ask Grevin to draft a reply to Sara's email about the invoice."
- "/mr-appdeen what happened in the Launch group this week?"
- "/appdeen-group Launch have hands turn the brief into a one-page PDF."

## What the connector reads and sends

Everything the plugin does goes through the one connector above; it fetches from no other address. Signing in lets Claude read, for the workspace you choose: the agents you may run, each agent's instructions and approved memory, your groups' briefs, timelines and files, the sources an agent's trainer gave it, and the services connected to an agent in AppDeen. Claude can record a task and what it came to in a group, keep a file there, propose a memory for an agent (its trainer approves it in AppDeen), and run a connected service's tool as the agent through Composio; a delete, or a message out when your workspace requires it, waits for your approval in AppDeen first, and tools that move money are refused. AppDeen keeps a log of each call: who, which tool, when, and whether it failed. It does not read your Claude conversations, files or memory.

Privacy policy: https://appdeen.ai/privacy. Terms: https://appdeen.ai/terms.

## Support

hello@appdeen.ai
