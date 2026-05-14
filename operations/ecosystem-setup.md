# Warrior X — Ecosystem Setup Guide

> This document records how the Warrior X ecosystem was established and serves as the canonical reference for setting up the ecosystem from scratch in any new environment.

---

## Overview

Warrior X is a citizen builder ecosystem hosted on GitHub under `andredavisme`. It provides structure, standards, and tooling for building community-focused software using AI, GitHub, and Supabase. It mirrors the operational flow of the 207 Analytix development environment, adapted for a citizen audience.

---

## Core Repos

| Repo | Purpose |
|---|---|
| `andredavisme/warrior-x-docs` | Ops hub, global training manual, ecosystem issue queue, standards |
| `andredavisme/skunk-works` | App features, frontend, UI development |
| `andredavisme/alexandria` | Database schemas, migrations, data pipelines |
| `andredavisme/alexandria-seed` | Consolidated 207 Analytix platform (5 source repos merged) |

## Ecosystem Repos (existing, scoped into Warrior X)

- andredavisme/parts-spec-matcher
- andredavisme/chronicle-worlds
- andredavisme/westbrook-city-band-platform
- andredavisme/maine-civic-tracker
- andredavisme/207analytix-sales-simulator
- andredavisme/newscapes-live
- andredavisme/social-app
- andredavisme/industrial-network-admin
- andredavisme/slate-booking

---

## Step-by-Step: Setting Up the Ecosystem

### Step 1 — Create Core Repos

Create the following repos on GitHub (autoInit: true):

```
warrior-x-docs   — Ops, docs, training manual
skunk-works      — Frontend, UI, app features
alexandria       — Database, schemas, migrations
alexandria-seed  — Consolidated platform repo (project-specific)
```

Optional (add when ready):
```
credential-broker — Credential and access management
```

### Step 2 — Seed warrior-x-docs

Push the following files to `warrior-x-docs` on `main`:

```
operations/training-manual.md         — Global citizen builder curriculum
operations/project-training-manual.md — warrior-x-docs specific manual
operations/ecosystem-setup.md         — This file
PROGRESS.md                           — Ecosystem progress log
```

Commit message: `docs: seed warrior-x-docs — global training manual and ecosystem setup`

### Step 3 — Seed Remaining Core Repos

For each of `skunk-works`, `alexandria`, `alexandria-seed`, push:

```
PROGRESS.md                      — Repo progress log
operations/training-manual.md    — Project-specific training manual
```

Commit message: `docs: seed PROGRESS.md and training-manual — Warrior X <repo-name>`

### Step 4 — Configure the Space

Create a Warrior X Space with the full Space instructions (see below). The Space serves as the combined:
- Ops queue assistant (fetches and sorts open issues each session)
- Task intake agent (converts raw input into GitHub issues)
- Standards enforcer (anchors all work to warrior-x-docs training manual)
- Manual maintenance agent (auto-updates training manuals via PR)

### Step 5 — Scope Existing Repos

For any existing repos to bring into the ecosystem:
1. Identify the repo and its purpose
2. Add it to the Space instructions repo list
3. Optionally seed with PROGRESS.md and operations/training-manual.md
4. Note it in warrior-x-docs/PROGRESS.md under Completed Milestones

---

## New Repo Protocol (ongoing)

Every time a new repo is created in the Warrior X ecosystem:

1. Create the repo on GitHub (autoInit: true)
2. Push to `main` in a single commit:
   - `PROGRESS.md` — using the standard structure
   - `operations/training-manual.md` — project-specific manual
3. Commit: `docs: seed PROGRESS.md and training-manual — Warrior X <repo-name>`
4. Add the repo to the Space instructions repo list
5. Note the new repo in `warrior-x-docs/PROGRESS.md` under Completed Milestones

### PROGRESS.md Structure

```markdown
# <Repo Name> — Progress Log

## Current Status
One-sentence summary of where the project stands right now.

## Active Work
What is currently in progress, by whom, and on which branch.

## Last Session
Date: YYYY-MM-DD
Summary of what was accomplished, decided, or discovered.
Overwrite this section each session — it reflects only the last session.

## Completed Milestones
Reverse-chronological list of completed work with dates.
Format: YYYY-MM-DD — <what was completed>

## Open Decisions
Questions not yet resolved. Remove items once decided.

## Blockers
Anything preventing forward progress. Remove when resolved.

## Next Steps
Ordered list of the next 3–5 concrete actions to take.

---
*Last updated: YYYY-MM-DD HH:MM EDT — <session summary in one line>*
```

### Project Training Manual Structure

```markdown
# <Repo Name> — Project Training Manual

> This manual covers what is unique to this repo.
> All global standards live in andredavisme/warrior-x-docs/operations/training-manual.md.

## What This Repo Is
## Who It Serves
## Tech Stack
## Key Conventions
## How to Contribute
## Security Rules
## Chapter 15 — Post-Mortems & Lessons Learned
```

---

## Manual Maintenance Protocol

The training manuals are living documents. When any of the following occur, update the relevant manual via PR:

- A new tool or platform is added to the stack
- A standard changes (commit format, naming, schema design)
- A new schema or migration pattern is established
- A security rule is decided
- A workflow step is clarified through practice
- An incident is resolved (add a post-mortem to Chapter 15)

Workflow:
1. Branch: `docs/auto-update-YYYYMMDD`
2. Edit only the relevant section
3. Commit: `docs: update training-manual — <brief description>`
4. Open a PR — do NOT merge, leave for André to review

---

*Last updated: 2026-05-14 07:22 EDT — Ecosystem setup guide created; full initialization documented*
