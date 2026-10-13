# AppDeen for Claude

AppDeen is where a company builds AI agents that hold its connected accounts, remember what they learn, and work in shared groups. This plugin brings those agents into Claude.

It adds the AppDeen connector (`https://mr.appdeen.ai/mcp/directory`), which you sign in to with your AppDeen account, and two skills:

- `handoff`: when you ask one of your agents for work ("ask Grevin to draft a reply to Sara"), Claude runs that agent in a subagent of its own, with the profile your organisation wrote for it.
- `/appdeen`: lists the agents you may run, or runs one by name (`/appdeen kanz which stores do you work with`).

## What the connector reads and sends

Signing in lets Claude read, for the workspace you choose: the agents you may run, each agent's instructions and approved memory, your groups' briefs, timelines and files, and the services connected to an agent in AppDeen. Claude can propose a memory for an agent (a person approves it in AppDeen) and run a connected service's tool as the agent, through Composio; a delete, or a message out when your workspace requires it, waits for your approval in AppDeen first, and tools that move money are refused. AppDeen keeps a log of each call: who, which tool, when, and whether it failed. It does not read your Claude conversations, files or memory.

## Support

hello@appdeen.ai
