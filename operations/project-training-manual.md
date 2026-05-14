# warrior-x-docs — Project Training Manual

> This manual covers what is unique to the warrior-x-docs repo. All global standards live in operations/training-manual.md in this same repo.

---

## What This Repo Is

warrior-x-docs is the operational hub of the Warrior X ecosystem. It is the source of truth for standards, conventions, and documentation that apply across all Warrior X projects. It also tracks the ecosystem-level issue queue and progress.

## Who It Serves

André and any contributors working within the Warrior X citizen builder ecosystem.

## Tech Stack

- Markdown (all documentation)
- GitHub (version control, issue tracking)
- No frontend, no database — this is a docs-only repo

## Key Conventions

- The global training manual lives at: `operations/training-manual.md`
- Per-repo training manuals live at: `operations/project-training-manual.md` in each repo
- The ecosystem progress log lives at: `PROGRESS.md` in this repo
- All updates to the training manual go through a PR — never commit directly to main
- Branch naming for manual updates: `docs/auto-update-YYYYMMDD`

## How to Contribute

1. Branch from main: `docs/auto-update-YYYYMMDD`
2. Edit only the section relevant to your change
3. Commit: `docs: update training-manual — <brief description>`
4. Open a PR and describe what triggered the update
5. Do NOT merge — leave for André to review

## What Belongs Here

- Global standards (commit formats, naming conventions, security rules)
- Ecosystem-level PROGRESS.md
- New repo seed protocol
- Post-mortems and lessons learned (Chapter 15 of training-manual.md)
- Decisions that affect more than one repo

## What Does NOT Belong Here

- Project-specific code or schemas
- Frontend files
- Database migrations

---

## Chapter 15 — Post-Mortems & Lessons Learned

*Ecosystem-level incidents and decisions get recorded here.*

---

*Last updated: 2026-05-14 — Initial project training manual seeded.*
