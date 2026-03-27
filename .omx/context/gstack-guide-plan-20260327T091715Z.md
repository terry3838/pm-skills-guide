# Context Snapshot: gstack-guide-plan

## Task Statement
Create a ralplan-grade execution plan for building a `gstack-guide` repository that:
- records the current repository structure first
- inspects `/home/terry/guide/origin/gstack` thoroughly
- writes a gstack usage guide into `/home/terry/guide/gstack-guide`
- initializes and publishes `gstack-guide` as a public git repository
- commits on `main` and pushes
- includes a Mermaid.js visualization strategy

## Desired Outcome
- A grounded PRD and test specification under `.omx/plans/`
- Clear document structure for `gstack-guide`
- A sequencing plan for repository setup, content migration, diagrams, and publication
- Explicit risks and prerequisites for the public push step

## Known Facts / Evidence
- The current repo is already a Markdown guide repository with a root `README.md`, category docs, an `assets/diagrams` directory, and a Mermaid rendering script via `npm run render:diagrams`. Evidence: `README.md`, `package.json`, `tools/render_diagrams.mjs`.
- `/home/terry/guide/gstack-guide` exists but is currently empty and is not a git repository.
- `/home/terry/guide/origin/gstack` is a sizable documentation + skills + browser tooling repository with `.agents/skills`, `browse/`, `extension/`, `docs/`, `scripts/`, `supabase/`, and test suites.
- gstack positions itself as a workflow stack with ordered phases: Think -> Plan -> Build -> Review -> Test -> Ship -> Reflect.
- gstack relies on generated `SKILL.md` files from templates and Bun-based build/test workflows.

## Constraints
- This turn is for planning, not direct implementation.
- The plan must be grounded in inspected repository facts, not assumptions.
- Consensus flow must run sequentially: Planner/draft, Architect, then Critic.
- Public repo creation/push likely depends on external Git hosting auth and may require manual/environment validation.

## Unknowns / Open Questions
- Which hosting target should receive the public remote for `gstack-guide` (likely GitHub, but not yet verified).
- Whether local GitHub CLI or existing auth is available for automated repo creation/push.
- The final scope of guide coverage: full repo deep dive vs onboarding-first guide with appendices.

## Likely Codebase Touchpoints
- `/home/terry/guide/pm-skills-guide/README.md`
- `/home/terry/guide/pm-skills-guide/package.json`
- `/home/terry/guide/pm-skills-guide/tools/render_diagrams.mjs`
- `/home/terry/guide/origin/gstack/README.md`
- `/home/terry/guide/origin/gstack/AGENTS.md`
- `/home/terry/guide/origin/gstack/ARCHITECTURE.md`
- `/home/terry/guide/origin/gstack/docs/skills.md`
- `/home/terry/guide/origin/gstack/package.json`
- `/home/terry/guide/gstack-guide`
