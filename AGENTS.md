# Repository instructions for AI agents

## Mission
Help develop a family of independent digital mathematics textbooks using the shared standards in this repository. Work autonomously within the task the user has authorized; do not require a new "continue" instruction for every routine step.

## Required orientation
Before changing files:
1. Read `README.md`, `AI_WORKFLOW.md`, `PRINCIPLES.md`, and the relevant standards under `docs/standards/`.
2. Identify whether the task belongs to the shared platform or to one specific book.
3. Inspect the existing implementation and recent history before proposing a new pattern.
4. State a concise plan for substantial work and then proceed unless a genuine decision or approval boundary is reached.

## Skill routing
Use the repository skill when the task matches:
- Writing, extending, or reviewing mathematical textbook content: `math-content-authoring`.
- Checking mathematical correctness, derivations, answers, domains, or solutions: `math-content-review`.
- Checking curriculum fit, progression, terminology, accessibility, or learning design: `pedagogical-review`.
- Building, validating, or visually inspecting a book: `book-build-qa`.

Skills are reusable procedures, not independent agents. Do not claim a separate agent or subagent ran unless the execution environment actually launched one.

## Execution model
- Complete all safe, in-scope steps in one work cycle: inspect, plan, implement, test, repair, retest, and report.
- Do not pause for routine confirmations such as "shall I continue?".
- Ask only when information is genuinely missing, requirements conflict, a material pedagogical/product decision is needed, or an action crosses an approval boundary.
- Explain important AI/tooling concepts briefly when they are encountered; the project uses a learn-by-building approach.
- Separate facts, assumptions, recommendations, and unverified claims.

## Quality gates
- Mathematical correctness, pedagogical suitability, visual rendering, and technical build quality are separate checks.
- Use deterministic tools (tests, scripts, symbolic computation) where suitable; do not rely only on model self-review.
- Inspect the rendered output for visual changes. A successful build is not proof of visual correctness.
- Report exactly which checks ran, their results, and any checks that could not be completed.
- Never claim a reviewer, skill, subagent, MCP server, or external tool was used unless it actually was.

## Git and approval boundaries
- Work on a dedicated branch and keep changes scoped.
- Review the diff and run relevant checks before preparing a pull request.
- Creating a branch, editing files, running tests, and opening a draft PR are permitted when included in the task.
- Do not merge, publish, deploy, delete user data, change access/permissions, or incur paid costs without explicit user approval.
- If an approval boundary is reached, finish all other safe work first and present one clear decision request.

## Handover
At completion report: objective, files changed, checks performed with evidence, remaining risks, and the exact human decision required (if any).
