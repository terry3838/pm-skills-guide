# PRD: gstack-guide Workflow Plan

## Requirements Summary

Build a Korean-first `gstack` usage guide in `/home/terry/guide/gstack-guide` by:
- recording the structure of the current guide repository first
- studying `/home/terry/guide/origin/gstack` in depth
- re-expressing the findings as a user-facing guide
- preparing a Mermaid-based visualization flow
- initializing and publishing the target as a public git repository on `main`

Grounding evidence:
- The current repository already uses a guide-oriented information architecture: root overview, progressive documents, category subdocs, and generated SVG diagrams from Markdown. See `/home/terry/guide/pm-skills-guide/README.md:7`, `/home/terry/guide/pm-skills-guide/README.md:145`, `/home/terry/guide/pm-skills-guide/package.json:5`, `/home/terry/guide/pm-skills-guide/tools/render_diagrams.mjs:8`.
- gstack itself is positioned as a multi-skill workflow system with quick start, install modes, sprint lifecycle, supporting docs, and technical internals. See `/home/terry/guide/origin/gstack/README.md:32`, `/home/terry/guide/origin/gstack/README.md:138`, `/home/terry/guide/origin/gstack/README.md:229`, `/home/terry/guide/origin/gstack/ARCHITECTURE.md:5`.
- gstack exposes 28 skills under `.agents/skills/`, generated skill docs, Bun-based build/test automation, and dedicated browser/test subsystems. See `/home/terry/guide/origin/gstack/AGENTS.md:7`, `/home/terry/guide/origin/gstack/AGENTS.md:34`, `/home/terry/guide/origin/gstack/package.json:10`, `/home/terry/guide/origin/gstack/docs/skills.md:5`.

## Acceptance Criteria

1. The plan records the current `pm-skills-guide` structure and uses it as the baseline template for the new guide repo.
2. The plan defines a concrete documentation IA for `gstack-guide`, including overview, installation, workflow, skill catalog, architecture, publication, and reference layers.
3. The plan explains how Mermaid source blocks will be authored and converted to SVGs in the target repo, reusing the proven renderer pattern from the current repo.
4. The plan includes a verified path for `git init`, `main` branch creation, first commit, public GitHub repo creation, and push.
5. The plan includes explicit verification steps for content completeness, diagram rendering, git state, and remote publication.
6. The plan includes follow-up staffing guidance for both sequential (`ralph`) and parallel (`team`) execution.

## RALPLAN-DR Summary

### Principles
- Reuse the proven guide shape before inventing a new one.
- Separate source-of-truth inspection from user-facing explanation.
- Prefer a hybrid guide: fast onboarding first, deep reference second.
- Treat diagrams as first-class documentation, not decoration.
- Keep publication steps explicit and verifiable because the target repo is currently empty.

### Decision Drivers
- The current guide repo already demonstrates a workable Markdown + generated-diagram pattern.
- gstack is large enough that a single linear README would collapse important distinctions between workflow, skills, architecture, and tooling internals.
- GitHub publication is feasible only if local auth and branch setup are handled as concrete steps.

### Viable Options

| Option | Pros | Cons |
|---|---|---|
| Mirror current guide repo one-to-one | Lowest structural risk, easy to render diagrams, familiar navigation model | May overfit the PM guide shape and bury gstack-specific workflows |
| Single long handbook | Fastest initial draft, minimal file count | Poor scanability, weak for 28-skill reference and architecture separation |
| Hybrid guide repo with root overview + focused deep dives | Preserves fast onboarding and supports deeper reference sections | Requires up-front IA work and disciplined content boundaries |

**Chosen direction:** Hybrid guide repo with root overview + focused deep dives.

## Proposed Information Architecture

Model the target repo on the current guide's root-overview pattern in `/home/terry/guide/pm-skills-guide/README.md:7` and `/home/terry/guide/pm-skills-guide/README.md:145`, but adapt the sections to gstack's lifecycle and repository anatomy from `/home/terry/guide/origin/gstack/README.md:138`, `/home/terry/guide/origin/gstack/README.md:229`, and `/home/terry/guide/origin/gstack/docs/skills.md:36`.

Planned document groups:
- Root overview: what gstack is, who it is for, quick-start path, repo map.
- Workflow docs: think/plan/build/review/test/ship lifecycle, review routing, team/parallel usage.
- Skill docs: grouped catalog for core workflow skills, power tools, and browser-centric skills.
- Technical docs: browser daemon architecture, generated SKILL.md pipeline, build/test commands, telemetry/privacy.
- Reference docs: glossary, installation matrix, command cheat sheets, troubleshooting, release/publishing notes.

Planned initial deliverables:
- A root overview that records the source repo map first, then reframes it as a user guide.
- A dedicated installation guide covering Claude-local, repo-local, and Codex-compatible install modes from `/home/terry/guide/origin/gstack/README.md:41` and `/home/terry/guide/origin/gstack/README.md:62`.
- A sprint workflow guide centered on `Think -> Plan -> Build -> Review -> Test -> Ship -> Reflect` from `/home/terry/guide/origin/gstack/README.md:138`.
- A skill-catalog guide grouped by workflow skills and power tools using `/home/terry/guide/origin/gstack/README.md:146` and `/home/terry/guide/origin/gstack/docs/skills.md:5`.
- A technical deep dive for the browser daemon and generated-doc pipeline using `/home/terry/guide/origin/gstack/ARCHITECTURE.md:7` and `/home/terry/guide/origin/gstack/ARCHITECTURE.md:179`.
- A publish/reference guide covering build, test, upgrade, telemetry, and troubleshooting from `/home/terry/guide/origin/gstack/AGENTS.md:34`, `/home/terry/guide/origin/gstack/package.json:10`, and `/home/terry/guide/origin/gstack/README.md:240`.

Planned target file tree:
- `README.md`
- `01-installation-and-setup.md`
- `02-sprint-workflow.md`
- `03-skill-catalog.md`
- `04-browser-and-architecture.md`
- `05-build-test-and-publish.md`
- `06-glossary-and-reference.md`
- `assets/diagrams/`
- `tools/render_diagrams.mjs`
- `package.json`

Target tooling contract for the first release:
- `package.json` declares the same Mermaid rendering dependency already proven in the current repo, `beautiful-mermaid`, so the target guide can render static SVGs with the same mechanism used in `/home/terry/guide/pm-skills-guide/package.json:5`.
- The target repo uses `npm` for the first release because this plan already expresses the render path as `npm run render:diagrams` and the current guide uses an npm-compatible script layout.
- The first local bootstrap must include dependency installation before any render verification.

## Implementation Steps

1. Record the current guide baseline.
   Use the existing shape in `/home/terry/guide/pm-skills-guide/README.md:145` and the rendered-diagram pipeline in `/home/terry/guide/pm-skills-guide/package.json:5` plus `/home/terry/guide/pm-skills-guide/tools/render_diagrams.mjs:8` as the reusable documentation template. Capture the baseline tree and note which pieces are structural versus PM-specific.

2. Build a gstack source map before writing any guide prose.
   Anchor the source inventory on `/home/terry/guide/origin/gstack/README.md:32`, `/home/terry/guide/origin/gstack/README.md:138`, `/home/terry/guide/origin/gstack/README.md:229`, `/home/terry/guide/origin/gstack/AGENTS.md:7`, `/home/terry/guide/origin/gstack/ARCHITECTURE.md:5`, and `/home/terry/guide/origin/gstack/docs/skills.md:5`. Summarize the repository by lanes: product/workflow narrative, skills catalog, browser subsystem, build/test toolchain, extension/sidebar, telemetry/deploy.

3. Bootstrap the target repo skeleton before long-form drafting.
   Initialize the empty target directory as a local repo on `main`, add the minimal documentation scaffold, and copy the proven Mermaid renderer pattern from `/home/terry/guide/pm-skills-guide/package.json:5` and `/home/terry/guide/pm-skills-guide/tools/render_diagrams.mjs:8`. Freeze the target tooling contract up front:
   - `package.json` exposes `render:diagrams`
   - `package.json` declares `beautiful-mermaid` so the renderer can execute without hidden dependency work
   - `tools/render_diagrams.mjs` scans Markdown and writes SVGs into `assets/diagrams/`
   - Mermaid source lives inline in Markdown fenced blocks until rendering replaces it with image links
   This sequence removes ambiguity later because diagram rendering in the target repo depends on having a package manifest, a renderer script, and an asset directory in place.

4. Draft the `gstack-guide` information architecture and core docs.
   Start with onboarding-first docs derived from gstack's quick start and sprint loop in `/home/terry/guide/origin/gstack/README.md:32` and `/home/terry/guide/origin/gstack/README.md:138`. Then add deep-reference layers for skill philosophy and architecture using `/home/terry/guide/origin/gstack/docs/skills.md:36` and `/home/terry/guide/origin/gstack/ARCHITECTURE.md:7`. Keep generated-doc conventions visible because skill docs are derived artifacts per `/home/terry/guide/origin/gstack/AGENTS.md:46`.

5. Render Mermaid diagrams as part of the authoring loop, not as a final afterthought.
   Reuse the current repository's `beautiful-mermaid` renderer flow from `/home/terry/guide/pm-skills-guide/package.json:5` and `/home/terry/guide/pm-skills-guide/tools/render_diagrams.mjs:23`. Author Mermaid source blocks in Markdown during drafting, run `npm run render:diagrams` before the first commit, and confirm the renderer writes SVGs into `assets/diagrams/`. Prioritize four diagram types because gstack explicitly emphasizes diagrams in planning and architecture: lifecycle flow, repository map, browser daemon architecture, and skill-category matrix. This aligns with gstack's own diagram-heavy planning stance in `/home/terry/guide/origin/gstack/docs/skills.md:145` and `/home/terry/guide/origin/gstack/ARCHITECTURE.md:11`.

6. Publish only after local verification passes.
   The target directory exists and is empty, and `gh auth status` confirms an authenticated `terry3838` GitHub session as of 2026-03-27. Use this exact runbook:
   - `git init`
   - `git branch -m main`
   - add the scaffold, docs, Mermaid assets, and toolchain files
   - `npm install`
   - run the diagram render command and inspect output
   - `git add .`
   - create the first commit on `main` using a Lore-protocol commit message required by this workspace
   - `gh repo create terry3838/gstack-guide --public --source . --remote origin`
   - `git push -u origin main`
   Because the current repo already uses HTTPS remotes, mirror that transport pattern for the new repo.

7. Run final content and publication verification.
   Before any push, validate that the written guide covers gstack's positioning, install modes, sprint flow, skills, architecture, build/test conventions, and privacy/telemetry claims grounded in `/home/terry/guide/origin/gstack/README.md:41`, `/home/terry/guide/origin/gstack/README.md:62`, `/home/terry/guide/origin/gstack/README.md:240`, `/home/terry/guide/origin/gstack/AGENTS.md:34`, and `/home/terry/guide/origin/gstack/package.json:10`. Then run `npm run render:diagrams`, git status checks, commit verification, `gh repo view`, and remote verification.

## Risks And Mitigations

| Risk | Why it matters | Mitigation |
|---|---|---|
| Source sprawl | gstack mixes workflow docs, generated skill docs, browser internals, and infra | Maintain a source map first and write by lane, not file order |
| Guide becomes a README rewrite | A direct translation of the root README would miss architecture and repository conventions | Split onboarding docs from deep technical references |
| Mermaid tool bootstrap gap | The render command will fail if the dependency and script contract are not created first | Explicitly add `beautiful-mermaid`, install dependencies, then render before commit |
| Mermaid drift | Diagram sources can diverge from rendered SVGs | Make rendering a repeatable script, not a manual export step |
| Publication order drift | Branch creation, commit timing, and remote creation can fail if done in the wrong order | Follow the explicit runbook and verify each transition before the next |
| Publication failure | Public repo creation depends on GitHub auth and remote wiring | Use `gh repo create --public`, verify remote, then push |
| Generated-doc confusion | Some gstack docs are generated from templates, not hand-edited | Call out generated vs source-of-truth artifacts explicitly in the guide |

## Verification Steps

1. Confirm the baseline repo shape still matches the current guide model by re-reading `/home/terry/guide/pm-skills-guide/README.md`, `/home/terry/guide/pm-skills-guide/package.json`, and `/home/terry/guide/pm-skills-guide/tools/render_diagrams.mjs`.
2. Confirm the gstack guide covers quick start, install variants, sprint flow, skill taxonomy, architecture, build/test commands, and privacy/telemetry against `/home/terry/guide/origin/gstack/README.md`, `/home/terry/guide/origin/gstack/AGENTS.md`, `/home/terry/guide/origin/gstack/ARCHITECTURE.md`, `/home/terry/guide/origin/gstack/docs/skills.md`, and `/home/terry/guide/origin/gstack/package.json`.
3. Render Mermaid diagrams successfully with zero skipped diagrams.
4. Verify the target repo installs cleanly and that `package.json` includes the expected Mermaid dependency before rendering.
5. Verify target repo state with `git status --short --branch`, `git branch --show-current`, `git log --oneline -1`, `git remote -v`, and `gh repo view`.
6. Verify the public remote shows the initial commit on `main`, the commit message follows the Lore protocol, and diagram assets are committed, not left untracked.

## ADR

### Decision
Build `gstack-guide` as a hybrid Markdown guide repository with onboarding-first root docs, deeper reference docs, and Mermaid-authored diagrams rendered to static SVGs.

### Drivers
- The current guide repo already proves the documentation + diagram workflow.
- gstack's source material spans multiple abstraction levels and needs layered exposition.
- GitHub publication is operationally straightforward in this environment because `gh` is installed and authenticated.

### Alternatives Considered
- Mirror-only structure: safer, but too rigid for gstack's architecture-heavy sections.
- Single-handbook structure: faster first pass, but weak navigation and poor maintainability.

### Why Chosen
The hybrid structure keeps the fastest path to understanding near the root while preserving room for detailed skill and architecture references. It also fits Mermaid-based visual aids cleanly.

### Consequences
- Requires a stronger IA pass before drafting.
- Produces more files than a single README, but the structure scales better.
- Makes diagram rendering part of the normal authoring loop.

### Follow-ups
- Create the target repo skeleton immediately after the source map, before long-form drafting.
- Decide the exact deep-dive file split after the source map is finished.
- Validate whether additional appendices are needed for browser commands or generated-template mechanics.
- Keep the publication order strict: render, commit, repo create, then push.

## Available-Agent-Types Roster

Practical roles for execution:
- `explore`: fast source mapping across current guide and origin/gstack
- `writer`: primary documentation drafting and restructuring
- `architect`: repo IA and technical section sanity review
- `executor`: repo bootstrap, git wiring, diagram tooling setup
- `verifier`: content coverage checks, diagram/render checks, git/remote verification
- `critic`: final plan/quality gate if scope changes during execution

## Follow-up Staffing Guidance

### Ralph Path
- Lane 1: `executor` with high reasoning for target repo bootstrap, file creation, git wiring, and Mermaid tooling
- Lane 2: `writer` with high reasoning for README and deep-dive documentation
- Lane 3: `verifier` with high reasoning for content coverage, diagram render, and publication proof

Why this works:
- The task is reversible and sequentially dependent: IA first, docs second, publish last.

### Team Path
- 1 `explore` low reasoning lane for source mapping and evidence tables
- 1 `writer` high reasoning lane for onboarding docs
- 1 `writer` high reasoning lane for technical/reference docs
- 1 `executor` medium/high reasoning lane for repo bootstrap and Mermaid tool wiring
- 1 `verifier` high reasoning lane for render/git/publication checks

Why this works:
- Source analysis, prose drafting, and repo/bootstrap tasks can overlap once the IA is fixed.

## Launch Hints

Sequential execution hint:
```bash
$ralph "Implement /home/terry/guide/pm-skills-guide/.omx/plans/prd-gstack-guide-workflow.md with /home/terry/guide/pm-skills-guide/.omx/plans/test-spec-gstack-guide-workflow.md, writing the guide into /home/terry/guide/gstack-guide and publishing it on GitHub."
```

Team execution hint:
```bash
$team "Execute the gstack-guide build from /home/terry/guide/pm-skills-guide/.omx/plans/prd-gstack-guide-workflow.md using /home/terry/guide/pm-skills-guide/.omx/plans/test-spec-gstack-guide-workflow.md. Split work into source mapping, onboarding docs, technical docs, repo bootstrap, and verification."
```

Alternate OMX launch hint:
```bash
omx team "Build /home/terry/guide/gstack-guide from the approved PRD and test spec, with lanes for mapping, writing, bootstrap, and verification."
```

## Team Verification Path

- `explore` proves source coverage with a mapped inventory of the current guide and origin/gstack.
- `writer` proves every major guide section is grounded in inspected source files.
- `executor` proves the target repo has a clean `main` branch, remote configured, and rendered diagrams committed.
- `verifier` proves the render script passes, git state is clean after commit, `gh repo view` resolves, and the public repo reflects the pushed content.

## Applied Improvements Changelog

- Added an explicit target file tree so execution does not have to infer the first repo shape.
- Tightened the publication sequence into a concrete `git init -> main -> render -> commit -> gh repo create -> push` runbook.
- Added Lore commit-protocol verification to the publication gate.
- Moved target repo bootstrap earlier so Mermaid tooling and asset paths exist before long-form drafting.
- Split local verification from publication so `gh repo create --public --source . --remote origin --push` happens only after a validated first commit.
- Added a more concrete initial deliverables set to reduce writer/executor guesswork during execution.
- Added an explicit Mermaid dependency/bootstrap step so `npm run render:diagrams` is actually executable in the target repo.
