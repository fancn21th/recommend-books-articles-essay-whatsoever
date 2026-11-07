# pstack on Codex

## Blog context and glossary

This project's resources and conversations provide material for the user's blog. Throughout each conversation, watch for concepts, terms, relationships, and context that would help the user understand or write about a resource later.

When useful material emerges, briefly point it out and suggest capturing it. Use the project-local `domain-modeling` skill to clarify and record resolved domain terminology in `GLOSSARY.md`. Keep broader source context and blog ideas separate from the glossary, and preserve references to their sources when available. Do not invent definitions or interrupt every exchange with a reminder.

Project-local pstack skills are in `.agents/skills/`, sourced from cursor/plugins pstack at commit `6b0300214a09fd6029cfb7077043125758cd1fd2`. Invoke a skill by name when relevant; `/poteto-mode` is the main entry point. Changes in this project take precedence over global skills of the same name.

These skills originated in Cursor. Interpret Cursor agent and tool references using available Codex tools and capabilities; do not assume Cursor plugins, models, slash commands, or automations are installed. Use the agent role descriptions in `pstack/agents/` as guidance when delegation is authorized and available. Follow the user's instructions and Codex tool and permission constraints whenever a skill conflicts with them. If an external dependency is unavailable, state the limitation and use an available equivalent where possible.

## pstack model configuration

Budget: medium (high). All roles use `inherit-parent`: omit the subagent model override; actual model and reasoning effort follow the parent session. This budget does not independently set the parent's reasoning effort.

- feature, refactoring: inherit-parent
- bug-fix: inherit-parent
- perf-issue: inherit-parent
- hillclimb: inherit-parent
- judgment and prose: inherit-parent
- hardest tasks: inherit-parent
- how explorer: inherit-parent
- how explainer: inherit-parent
- why investigators: inherit-parent
- why synthesizer: inherit-parent
- reflect tooling: inherit-parent
- reflect judgment, divergent, synthesizer: inherit-parent
- arena runners: inherit-parent, inherit-parent
- arena cross-judge pool: inherit-parent
- swarm workers: inherit-parent
- architect runners: inherit-parent, inherit-parent
- interrogate reviewers: inherit-parent, inherit-parent

Panel entries specify the number of agents when delegation is authorized and available. An inherit-parent entry cannot serve as an arena cross-judge; no cross-family judge is configured.
