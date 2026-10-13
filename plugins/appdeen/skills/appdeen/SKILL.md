---
name: appdeen
description: Run one of your AppDeen agents by name, or list them. Type /appdeen followed by the agent and the task, or /appdeen alone.
argument-hint: "[agent] [task]"
disable-model-invocation: true
---

The person typed: $ARGUMENTS

Use the AppDeen connector.

- Nothing typed: call `list_agents` and show the agents as a short list, each with one line on what it does, then ask which one and what for.
- An agent named with a task: run that agent on the task as the AppDeen connector describes.
- An agent named with no task: ask what it should do.
- A name that matches no agent: call `list_agents` and offer the closest ones.

When the AppDeen connector is not connected, say so and give this link to add it: https://claude.ai/customize/connectors?modal=add-custom-connector&connectorName=AppDeen&connectorUrl=https%3A%2F%2Fmr.appdeen.ai%2Fmcp
