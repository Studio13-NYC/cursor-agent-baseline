# cursor-agent-baseline

**Active development:** this repo is a work in progress. Paths, prompts, and conventions will shift; expect rough edges and broken assumptions until things stabilize.

## What this is

A **Cursor-oriented baseline** for multi-agent style workflows: agent ownership files, shared rules, and small reusable skills you can copy into a project and refine. It is a starting point for teams that want clearer boundaries between general implementation and specialist layers (UI, API, graph, LLM, QA, DevOps, design) without committing to a particular application stack.

### It includes

* `AGENTS.mdc` (repository root — Cursor agent instructions)
* `.cursor/agents/*.mdc`
* `.cursor/rules/global/*.mdc`
* `.cursor/rules/engineering/*.mdc`
* `.cursor/skills/**/SKILL.md`

### Design choices

* **Agents** are ownership-based (who owns which kind of work).
* **Rules** are minimal shared constraints and engineering standards.
* **Skills** are reusable execution modules (procedures the agent can follow).
* **Development** is treated as the generalist implementer.
* **UI / API / graph / LLM / QA / DevOps / design** are specialist owners.
* **Architecture** protects cross-layer structure.
* **Orchestrator** routes and coordinates.

### Next iteration (highest value)

If you want the next refinement, the highest leverage is to make the agent files **more Cursor-specific** by adding:

* explicit invocation triggers
* preferred output format
* escalation rules
* examples of when to defer to another agent
