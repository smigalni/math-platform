# AI development system

## Purpose
Provide a practical, reusable AI-assisted engineering workflow for `matte`, `tmatte`, and future book repositories while preserving their independence.

## Architecture

| Layer | Responsibility | Current implementation |
|---|---|---|
| Repository policy | Persistent rules and approval boundaries | Root `AGENTS.md` |
| Skills | Reusable task procedures loaded when relevant | Repo-local skills under `.agents/skills/` |
| Role profiles | Define specialist responsibilities and review criteria | Documented in `.agents/roles/` |
| Orchestration | Plan work, select skills/roles, sequence tasks, consolidate findings | Currently performed by the active coding agent; no dedicated orchestrator service yet |
| Tools | Git, build/test commands, Python/SymPy, browser automation, APIs | Use only tools actually available in the execution environment |
| MCP | Standardized access to external tools and data | Not configured in this repository yet |
| Harness | Instructions, skills, tools, permissions, execution environment, context and verification loop | Initial repository-level harness is being established |
| CI | Repeatable automated checks on changes | Existing book-specific GitHub Actions remain owned by each book |

## Important distinctions
- An **agent** is an executing model instance with a goal, instructions, tools and boundaries.
- A **subagent** is a separately launched agent delegated a bounded task, usually with its own context and returned findings.
- A **skill** is a reusable procedure/instruction package. A skill does not execute independently.
- **MCP** is a protocol for exposing tools and resources to an agent. It is not itself an agent or an orchestrator.
- A **harness** is the surrounding execution system: model, instructions, tools, permissions, context management, runtime and verification.
- **CI** runs configured automation; it is not automatically an AI agent.

## Specialist roles
The role profiles in `.agents/roles/` define responsibilities for content authoring, mathematical review, pedagogical review and technical QA. They can be used as delegation briefs when the runtime supports subagents. Until then, the main agent can apply them sequentially as distinct review passes. Reports must not imply independent review if the passes were performed by the same model/context.

## Autonomy and human control
The agent should autonomously complete routine in-scope work, including inspection, editing, tests, fixes and retesting. Human review is required for material changes to curriculum or product direction and before merge, publication, deployment, permissions changes or paid services.

## Rollout
1. Establish repository instructions and a small set of high-value skills.
2. Pilot the workflow on an existing chapter in a book repository without coupling that book to this repository at build time.
3. Add deterministic validators where repeated failures justify them.
4. Add an actual multi-agent runtime only when it provides independent review or parallel execution worth its complexity.
5. Evaluate MCP integrations against concrete tool-access needs; do not add servers speculatively.
6. Keep book repositories independently buildable and publishable.
