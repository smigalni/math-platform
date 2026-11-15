---
name: book-build-qa
description: Validate a mathematics book after content, navigation, styling or configuration changes. Use when building, testing, checking links or reviewing rendered pages.
---

# Book build and QA

## Preflight
- Read the book's own build instructions and identify its actual build/test commands.
- Identify changed pages, shared components, navigation and assets.
- Determine whether the change requires content, link, accessibility, responsive or print checks.

## Validation
1. Run the documented quality checks and production build.
2. Check exit codes and inspect relevant logs; do not infer success from a started workflow.
3. Check internal links, navigation and referenced assets in the affected scope.
4. Inspect generated HTML for structural errors when useful.
5. Visually inspect the built pages at relevant viewport sizes when browser tooling is available.
6. Check mathematical rendering, code blocks, tables, admonitions, answer styling and page breaks when affected.
7. For print-related changes, inspect print/PDF output if the environment supports it.

## Evidence and limits
Report commands, exact outcomes and scope. Distinguish build success, structural checks and visual review. If browser access or a renderer is unavailable, say so explicitly and leave visual QA incomplete. Do not claim a page was visually inspected based only on its source or generated HTML.
