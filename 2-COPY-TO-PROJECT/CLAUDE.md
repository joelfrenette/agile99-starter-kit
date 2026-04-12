# CLAUDE.md — Agile99 Project Rules for Claude Code
# Place in your project root. Claude Code reads this at the start of every session.
# Also works with: Antigravity (supplemental), GitHub Copilot (as AGENTS.md)

## Confirmation required (non-negotiable)
At the start of every chat output:
"AI_RULES.md OK | CONTEXT.md OK | Phase: [X] | Goal: [X]"
Do not write any code before this confirmation.

## Project
Name:   [YOUR APP NAME]
Stack:  [e.g. Next.js, Supabase, Vercel, Tailwind]
Repo:   github.com/[YOUR-HANDLE]/[YOUR-REPO]
Deploy: Vercel (dev branch = staging, main = production)
Tracker: PROJECT-TRACKER.md (update at end of every session)

## Simplified Branching (DEV -> UAT -> Main)
Two branches per feature cycle. That is all.

  dev/[feature-name]   <- all development work
      Morpheus intake -> epics/stories -> build -> code
      Auto-QA runs here before promoting to UAT

  uat/[sprint-name]    <- testing and acceptance
      Auto-generated UAT test plan lives here
      UAT checklist must be 100% before merging to main

  main                 <- production (always live, always clean)

Do NOT create more than 2 branches per feature cycle.
Do NOT merge to main without a completed UAT checklist.

## Session Flow (replaces A Feature in Five)
Every session follows this simple loop:

  1. INTAKE  -- Morpheus interviews Neo, collects requirements as epics/stories
  2. PLAN    -- Oracle converts stories to tasks, updates PROJECT-TRACKER.md
  3. BUILD   -- The Architect designs, Cypher codes on dev/[name] branch
  4. QA      -- Trinity runs auto-QA, generates UAT test plan, promotes to uat/
  5. SHIP    -- Tank merges uat/ to main after Neo approves UAT checklist
  6. TRACK   -- PROJECT-TRACKER.md updated, KPIs recalculated

## Auto-QA Requirements (mandatory before UAT promotion)
Before any branch is promoted to UAT, the AI must:
  1. Generate a test plan covering: happy path, 3 edge cases, 2 failure modes
  2. Output a clickable UAT checklist (markdown format with [ ] checkboxes)
  3. Note the checklist filename: UAT-[sprint]-[date].md
  4. Update PROJECT-TRACKER.md with the new UAT branch and test count

## Epic and Story Format (Morpheus auto-creates these)
Epic:  [EPIC-N] [Name] -- [one sentence description]
Story: [EPIC-N]-[S] As a [user], I want [action], so that [outcome]
Task:  [EPIC-N]-[S]-[T] [specific implementation task] -- Est: [S/M/L]

## Non-negotiable coding rules
- All API routes must use withErrorHandler() wrapper
- All protected routes must use requireAuth() middleware
- Never write to database from client-side code
- Never hardcode secrets -- use environment variables only
- No console.log in production code
- Output only modified files -- never the full project
- State what you will NOT touch before coding anything
[ADD YOUR OWN RULES HERE AS YOU DISCOVER THEM]

## End of every session (mandatory)
1. Output full updated CONTEXT.md
2. Update PROJECT-TRACKER.md with session progress
3. Note what worked/failed -> PROMPT-LOG.md
4. State exact starting point for next session
5. If dev work done: output UAT test plan and checklist

## Rule change log
[DATE] v2.0 - Simplified to DEV/UAT/Main branching
[DATE] v2.0 - Added auto-QA and UAT checklist generation
[DATE] v2.0 - Added PROJECT-TRACKER.md update requirement
