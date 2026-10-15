---
name: appdeen-group
description: Work inside one of your AppDeen groups, or list them. Type /appdeen-group followed by the group and what to do, or /appdeen-group alone.
argument-hint: "[group] [task]"
disable-model-invocation: true
---

The person typed: $ARGUMENTS

Use the AppDeen connector.

- Nothing typed: call `list_groups` and show the groups, one line each with its overview and last activity, then ask which one.
- A group named (match it ignoring case against `list_groups`): read it with `group_overview`. With a task, do it there: an agent's task is recalled with that group (`recall` with `group`), so it is recorded in it, and any file made is kept there with `save_to_group` (that group). Without a task, say in a few lines where the group stands and what is open.
- A name that matches no group: show the closest ones from `list_groups`.

When the AppDeen connector is not connected, say so and give this link to add it: https://claude.ai/customize/connectors?modal=add-custom-connector&connectorName=AppDeen&connectorUrl=https%3A%2F%2Fmr.appdeen.ai%2Fmcp%2Fdirectory
