# Warrior X — Citizen Builder Training Manual

> *You don't have to be a developer to build something that matters. You just have to start.*

This manual is your guide to using AI, GitHub, and Supabase to create real tools that help your community solve real problems. It is written for complete beginners. Every chapter builds on the last. Take it one step at a time.

---

## Chapter 1 — Welcome to Warrior X

### What This Is
Warrior X is a community of builders. Not professional developers — citizens. People who see a problem in their neighborhood, their school, their city, and decide to do something about it.

The tools we use — AI, GitHub, and Supabase — are free or low-cost and powerful enough to build real software. The skills you learn here are the same ones used by professionals around the world.

### What You Will Build
By the end of this curriculum you will have:
- Used AI to help you think, write, and code
- Created and managed a real project on GitHub
- Built a live database with Supabase that stores and serves real data
- Shipped at least one tool your community can actually use

### The Three Pillars
| Pillar | Tool | What It Does For You |
|---|---|---|
| Think & Create | AI (Perplexity, ChatGPT, etc.) | Helps you plan, write, and generate code |
| Organize & Ship | GitHub | Stores your work, tracks changes, enables collaboration |
| Store & Serve | Supabase | Holds your data and makes it available to your app |

---

## Chapter 2 — Your Mindset as a Builder

### You Are Not Learning to Be a Programmer
You are learning to be a **builder**. The difference matters. Programmers write code from memory. Builders use every tool available — including AI — to bring ideas to life. Your job is to know what you want to build and how to guide the tools that help you build it.

### Mistakes Are Progress
Every error message, broken link, and failed deployment is information. It is telling you something. Nothing you do here will break the internet. You can always undo, reset, and try again.

### Community First
Every tool you build should answer one question: *Who does this help?* Keep your community at the center of every decision.

---

## Chapter 3 — Getting Set Up

### What You Need
- A computer with internet access
- A free GitHub account — sign up at [github.com](https://github.com)
- A free Supabase account — sign up at [supabase.com](https://supabase.com)
- Access to a free AI assistant (Perplexity, ChatGPT, or similar)
- A text editor — [VS Code](https://code.visualstudio.com) is recommended and free

### Your First GitHub Repository
A repository (repo) is like a folder for your project — but smarter. It remembers every change you ever make.

1. Log into GitHub
2. Click the **+** button in the top right → **New repository**
3. Give it a name related to your project (example: `community-food-map`)
4. Check **Add a README file**
5. Click **Create repository**

Congratulations — you just created your first project home.

---

## Chapter 4 — Working with AI

### AI Is Your Thinking Partner
AI assistants are not magic and they are not always right. Think of them as a very knowledgeable collaborator who needs your direction. The better you describe what you want, the better the output.

### How to Ask AI for Help
Be specific. Include:
- What you are building
- Who it is for
- What you want the AI to help with right now

**Weak prompt:** *"Help me make a website"*
**Strong prompt:** *"I am building a community food pantry locator for Portland, Maine. Help me write the HTML for a simple search page where someone can enter their zip code and see nearby pantries."*

### What AI Is Great At
- Explaining concepts in plain language
- Writing and editing code
- Helping you think through a problem step by step
- Drafting content, labels, and descriptions
- Debugging errors when you paste them in

### What AI Gets Wrong
- Specific local facts (always verify)
- Very recent information
- Your exact project context (you must provide it each session)

### Golden Rule
Never paste a secret (password, API key, private token) into an AI chat. Ever.

---

## Chapter 5 — GitHub Fundamentals

### Key Concepts

**Repository** — Your project's home. All files and history live here.

**Branch** — A safe copy of your project where you can make changes without affecting the main version. Always work on a branch.

**Commit** — A saved snapshot of your changes. Write a short message describing what you did.

**Pull Request (PR)** — A proposal to merge your branch into the main project. This is where review and discussion happen.

**Merge** — Accepting a pull request and bringing the changes into main.

### The Warrior X Workflow
Every change follows this path — no exceptions:

```
branch → commit → push → pull request → review → merge
```

Never commit directly to `main`. Always branch first.

### Commit Message Format
Write commit messages that explain *what* you did:

```
feat: add zip code search to food pantry map
fix: correct broken link on homepage
docs: update README with setup instructions
```

Types to use: `feat` | `fix` | `docs` | `schema` | `chore` | `refactor`

### Issues — Your Task List
GitHub Issues are how we track work. Every task gets an issue. Every issue has:
- A clear, action-oriented title
- A description of what needs to be done
- A checklist of concrete steps
- An owner (who is doing it)

---

## Chapter 6 — Supabase Fundamentals

### What Is Supabase?
Supabase is your project's database and backend. It stores information — names, locations, events, responses — and makes that information available to your app in real time. It is free to start and built on open-source technology.

### Key Concepts

**Project** — Your Supabase workspace. One project per app.

**Table** — Like a spreadsheet. Rows are records, columns are fields. Example: a `pantries` table might have columns for `name`, `address`, `hours`, and `zip_code`.

**Row Level Security (RLS)** — Rules that control who can see or edit which data. **RLS must be enabled on every table you create.** This is not optional.

**API Key** — A password that lets your app talk to your database. There are two kinds:
- **Anon key** — Safe to use in your frontend app
- **Service role key** — Never use this in frontend code. Ever.

### Storing Secrets Safely
API keys and passwords never go in GitHub. Store them in:
- Supabase Vault (for database secrets)
- Environment variables in your hosting platform

### Your First Table
1. Open your Supabase project
2. Go to **Table Editor** → **New Table**
3. Name your table (example: `locations`)
4. Add columns for the data you need
5. Enable **Row Level Security** before saving
6. Set policies for who can read and write

---

## Chapter 7 — Building Your First Tool

### Start With the Problem
Before writing a single line of code, answer these three questions:
1. What problem does this solve?
2. Who will use it?
3. What is the simplest version that would actually help?

That simplest version is your **MVP** — Minimum Viable Product. Build that first.

### The Build Loop
Every feature follows this cycle:

1. **Define** — Write a GitHub issue describing what you're building
2. **Design** — Sketch it out (even on paper)
3. **Ask AI** — Use your AI assistant to help generate the code
4. **Build** — Paste and adapt the code in your editor
5. **Test** — Does it work? Does it break anything?
6. **Commit** — Save your work with a clear commit message
7. **Ship** — Open a PR, review, merge

### Project Naming Conventions
- Repo names: lowercase, hyphenated (example: `food-pantry-map`)
- Migration files: `YYYYMMDD_NNN_description.sql` (example: `20260514_001_create_locations_table.sql`)
- Branch names: descriptive (example: `feat/add-zip-search`)

---

## Chapter 8 — Collaboration

### Working With Others
Warrior X is built on collaboration. When working with teammates:
- Assign issues clearly — one owner per task
- Use PRs for all changes so teammates can review
- Leave comments on PRs when you have questions or suggestions
- Never merge your own PR without a second set of eyes when possible

### Communication Standards
- Keep issue descriptions factual and actionable — no meeting notes or chat context
- One task per issue — never combine unrelated work
- If a task is blocked, say so in the issue and tag who can unblock it

---

## Chapter 9 — Security Rules (Non-Negotiable)

These rules protect you, your community, and the people whose data you steward.

- 🔴 **No secrets in GitHub** — API keys, passwords, and tokens go in the Supabase Vault or environment variables only
- 🔴 **RLS on every table** — No exceptions. Every table needs row level security enabled
- 🔴 **Never use the service role key in frontend code** — Use the anon key only
- 🔴 **No direct commits to main** — Always branch → PR → merge
- 🟡 **Review before merging** — At least one other person should review significant changes

---

## Chapter 10 — Your First Community Project Checklist

Use this checklist when starting any new project:

- [ ] Defined the problem and the community it serves
- [ ] Created a GitHub repository with a clear name and README
- [ ] Created a Supabase project
- [ ] Designed the data model (what tables and columns do you need?)
- [ ] Created tables with RLS enabled
- [ ] Built an MVP — the simplest useful version
- [ ] Tested with at least one real person from the community
- [ ] Opened issues for next steps
- [ ] Shared the project with at least one other Warrior X builder

---

## Chapter 11 — Glossary

| Term | Plain Language Definition |
|---|---|
| Repository (repo) | A folder that tracks every change to your project |
| Branch | A safe copy to work on without affecting the main project |
| Commit | A saved snapshot with a description of what changed |
| Pull Request | A proposal to add your changes to the main project |
| Merge | Accepting a pull request |
| Issue | A task or bug tracked in GitHub |
| Table | A structured set of data in Supabase (like a spreadsheet) |
| RLS | Row Level Security — controls who can access which data |
| API Key | A password your app uses to talk to a service |
| MVP | Minimum Viable Product — the simplest version that works |
| Migration | A versioned file that changes your database structure |

---

## Chapter 12 — Resources

- **GitHub Docs** — [docs.github.com](https://docs.github.com)
- **Supabase Docs** — [supabase.com/docs](https://supabase.com/docs)
- **VS Code** — [code.visualstudio.com](https://code.visualstudio.com)
- **Perplexity AI** — [perplexity.ai](https://perplexity.ai)

---

## Chapter 15 — Post-Mortems & Lessons Learned

*This chapter grows over time. When something breaks, when a decision is reversed, or when a pattern proves itself in practice — it gets recorded here so the whole community learns from it.*

---

### PM-001 — AI Sandbox Filesystem Path Assumptions (2026-05-15)

**Project:** EIA Schneider Training Portal
**Severity:** Medium — blocked file generation for one session, no data lost

#### What Happened
During a session to generate the training portal front-end HTML, two file-write commands failed:

1. `mkdir -p ~/training-portal` — failed silently because `~` resolved to `/home/user/`, a path that does not exist in this sandbox environment.
2. `mkdir /root/training-portal` — returned `Permission denied` because the sandbox user has no write access to `/root/`.

The session stalled. No files were generated or shared.

#### Root Cause
The AI sandbox filesystem does not follow a standard Linux home directory layout. The writable working directory is at a different path than `~` or `/root/`. Assuming the path without confirming it first caused both commands to fail.

#### Fix
Begin every file-writing session with:

```bash
echo $HOME && pwd
```

This confirms the actual writable path before any `mkdir` or file-write commands. Once confirmed, all file generation and `share_files` delivery works normally.

#### Rule Added
> **Always confirm the sandbox path before writing files.** Run `echo $HOME && pwd` as the first command of any file-generating session. Never assume `~` or `/root/` are valid writable paths in the AI sandbox environment.

---

*Last updated: 2026-05-15 14:00 EDT — Added PM-001: AI sandbox path diagnosis from eia-schneider-training-portal session.*
