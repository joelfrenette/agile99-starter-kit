STEP 2 — COPY THESE FILES TO YOUR PROJECT
==========================================
The files you need depend on which tool you are using.

ALL TOOLS — always copy these 2 files to your project root:
  CONTEXT.md       <- your living project brain
  PROMPT-LOG.md    <- your self-improving prompt log

THEN copy the rules file for your specific tool:

V0.APP:
  Copy AI_RULES.md to your project root.
  Push all 3 files to GitHub. V0 reads from the connected repo.

DYAD.SH:
  Copy AI_RULES.md to your project root folder on your machine.
  Overwrites Dyad's default AI_RULES.md (click YES to overwrite).
  Dyad reads it automatically every chat.

WINDSURF:
  Copy .windsurfrules to your project root folder.
  Windsurf's Cascade AI reads it automatically every session.

VS CODE + GITHUB COPILOT:
  Copy the .github/ folder to your project root.
  It contains copilot-instructions.md inside it.
  Copilot reads it automatically for every chat request in VS Code.

CURSOR:
  Copy the .cursor/ folder to your project root.
  It contains rules/agile99.mdc (alwaysApply: true).
  Cursor reads it automatically every session.
  (Also .cursorrules is included for older Cursor versions.)

See START-HERE.html for step-by-step setup for each tool.
