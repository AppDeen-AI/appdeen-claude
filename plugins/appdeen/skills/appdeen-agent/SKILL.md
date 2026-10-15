---
name: appdeen-agent
description: Run one of your AppDeen agents by name, or pick one from a card. Type /appdeen-agent followed by the agent and the task, or /appdeen-agent alone.
argument-hint: "[agent] [task]"
disable-model-invocation: true
---

The person typed: $ARGUMENTS

Use the AppDeen connector.

- Nothing typed: call `show_agents`, which shows the person a card of their agents to pick from. Add nothing after it.
- An agent named with a task: fetch its profile with `recall` (the agent and the task; `group` when the person names one, else it is recorded in their Unfiled), then launch one subagent with the Agent tool, subagent_type general-purpose, whose prompt is the profile followed by the task. Show its reply and share any file it made. When it is done, call `report_task` with the task id recall gave and what was done, and keep its files in the same group with `save_to_group`.
- An agent named with no task: ask what it should do.
- A name that matches no agent: call `list_agents` and offer the closest ones. A request that names no agent belongs to /mr-appdeen: do what it does.

When the AppDeen connector is not connected, say so and give this link to add it: https://claude.ai/customize/connectors?modal=add-custom-connector&connectorName=AppDeen&connectorUrl=https%3A%2F%2Fmr.appdeen.ai%2Fmcp%2Fdirectory
