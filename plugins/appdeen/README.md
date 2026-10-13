# AppDeen for Claude

AppDeen is where a company builds AI agents that hold its connected accounts, remember what they learn, and work in shared groups. This plugin brings those agents into Claude.

It adds the AppDeen connector (`https://mr.appdeen.ai/mcp`), which you sign in to with your AppDeen account, and one command:

- `/appdeen` lists the agents you may run.
- `/appdeen grevin draft a reply to Sara` runs Grevin on that task.

You can also just ask: "ask Kanz which Shopify stores he works with".

## What the connector reads and sends

Signing in lets Claude read, for the workspace you choose: the agents you may run, each agent's instructions and approved memory, your groups' briefs, timelines and files, and the services connected to an agent in AppDeen. Claude can propose a memory for an agent (a person approves it in AppDeen) and run a connected service's tool as the agent; a delete or a message out waits for your approval in AppDeen first. AppDeen keeps a log of each call: who, which tool, when, and whether it failed. It does not read your Claude conversations, files or memory.

## Support

hello@appdeen.ai
