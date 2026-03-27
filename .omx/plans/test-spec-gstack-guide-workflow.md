# Test Spec: gstack-guide Workflow

## Goal

Verify that execution of the `gstack-guide` plan produces a usable, publishable guide repository with correct source grounding, rendered diagrams, and a public GitHub remote on `main`.

## Test Matrix

| Area | Check | Method | Pass Condition |
|---|---|---|---|
| Baseline capture | Current guide structure is recorded before writing | Compare execution notes against `/home/terry/guide/pm-skills-guide/README.md:145` and current repo tree | The baseline tree and reusable patterns are documented |
| Source coverage | gstack analysis spans workflow, skills, architecture, build/test, and privacy | Cross-check citations against `/home/terry/guide/origin/gstack/README.md`, `/home/terry/guide/origin/gstack/AGENTS.md`, `/home/terry/guide/origin/gstack/ARCHITECTURE.md`, `/home/terry/guide/origin/gstack/docs/skills.md`, `/home/terry/guide/origin/gstack/package.json` | No major source lane is missing |
| Guide IA | Target repo includes overview, workflow, skills, architecture, and references | Inspect written Markdown tree in `/home/terry/guide/gstack-guide` | `README.md`, `01-installation-and-setup.md`, `02-sprint-workflow.md`, `03-skill-catalog.md`, `04-browser-and-architecture.md`, `05-build-test-and-publish.md`, and `06-glossary-and-reference.md` all exist and are readable |
| Dependency bootstrap | Mermaid renderer dependency and script contract are present | Inspect target `package.json` and install output | `beautiful-mermaid` is declared and dependency installation succeeds before render |
| Diagram pipeline | Mermaid blocks render to SVG assets | Run `npm run render:diagrams` in the target repo | Zero skipped diagrams and generated assets present |
| Git bootstrap | Repo initialized on `main` with initial Lore commit | `git status --short --branch`, `git log --oneline -1`, `git log -1 --format=%B` | Branch is `main`, working tree is clean, initial commit exists, and the commit body follows the Lore protocol |
| GitHub publication | Public remote exists and matches local repo | `git remote -v`, `gh repo view`, push result | Public repo resolves and `origin` points to it |

## Execution Checks

1. After source mapping, verify the execution notes include the current guide structure and a gstack source inventory.
2. After documentation drafting, verify the target repo contains both onboarding and deep-reference docs.
3. Before diagram rendering, verify `package.json` declares `beautiful-mermaid` and dependency installation succeeds.
4. After diagram setup, run `npm run render:diagrams` and check the generated SVG directory.
5. After git bootstrap, verify `main` exists locally, the first commit is present, and the commit message includes Lore trailers.
6. After GitHub creation and push, verify the remote repo is public and reachable.

## Failure Conditions

- The target repo is still empty after the documentation phase.
- The guide only paraphrases the gstack root README and omits architecture or skill-deep-dive context.
- The target repo declares a render command but cannot install or execute the Mermaid dependency.
- Mermaid rendering is not automated or leaves skipped diagrams unresolved.
- The repo is initialized but not pushed publicly.
- Publication succeeds but the local branch is not `main`.

## Evidence To Collect

- Final target repo tree
- Render command output
- Dependency install output
- `package.json` script definition for `render:diagrams`
- `git status --short --branch`
- `git remote -v`
- `gh repo view` output
- The public repository URL
