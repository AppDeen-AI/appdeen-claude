---
name: handoff
description: Hand a message to one of the person's AppDeen agents whenever they address an agent of theirs by name, with a task or a question, such as "ask Grevin to draft a reply", "have hands make a PDF" or "Kanz, which stores do you work with?".
---

Whenever the person addresses one of their AppDeen agents, with a task or a question, that agent answers in a subagent of its own:

1. Call AppDeen's `recall` with the agent's name and the message in the person's words. It returns the profile the person's organisation wrote for that agent; the name matches ignoring case.
2. Launch one subagent with the Agent tool, subagent_type general-purpose, whose prompt is that profile, a blank line, then "The task:" and the message.
3. Show the subagent's reply as it returns, and share any file it made. Do not answer for the agent yourself.

Call `list_agents` only when it is unclear which agent is meant, then pick the one whose description fits, or ask.
