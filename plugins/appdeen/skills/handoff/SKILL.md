---
name: handoff
description: Hand work to one of the person's AppDeen agents when they ask an agent of theirs by name, such as "ask Grevin to draft a reply" or "have hands make a PDF".
---

When the person asks one of their AppDeen agents for work, that agent does it in a subagent of its own:

1. Call AppDeen's `recall` with the agent's name and the task in the person's words. It returns the profile the person's organisation wrote for that agent.
2. Launch one subagent with the Agent tool, subagent_type general-purpose, whose prompt is that profile, a blank line, then "The task:" and the task.
3. Show the subagent's reply as it returns, and share any file it made.

When the name is unclear, call `list_agents` first and pick the agent whose description fits, or ask.
