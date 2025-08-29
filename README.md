# Context Engineering

Context Engineering repository: protocol documents and templates for iterative, module-driven app construction by an AI-assisted engineer.

## What this repo is
A small collection of protocol documents, templates, and examples that define how an AI engineer (e.g., Code Shield / Cipher Gear) should operate when building applications one functional unit at a time, with mandatory user verification.

<!-- Inspired by -->
**Inspired by:** https://github.com/Pythonation/Context-Engineering-for-AI-Coding/blob/main/README.md

## Key files
- Copilot_context.md — Code Shield-2 (VSCode Copilot Edition) protocol (safe-edit rules, Copilot guidance).
- Gimini_context-en-2.md — Code Shield-1 protocol (Gemini edition).
- Gimini_context-ar.md — Arabic version of the protocol.
- product_roadmap.md — Product roadmap template to be used in Phase 1.
- LICENSE — Apache License 2.0.

## Quick usage
1. Phase 1 — Foundation & Verification
   - User and agent draft research, fact & inspiration searches (English-only).
   - Agent prepares the Product Roadmap using the provided template (product_roadmap.md).
   - Mandatory stop: the agent must request and wait for explicit user approval before writing any files.

2. Phase 2 — Module-Based Construction
   - Build one functional module at a time.
   - For every modified file, follow the Mandatory Safe-Edit Protocol:
     1. Read the file.
     2. Announce the edit plan and precise anchor point.
     3. Edit only at the anchor point (preserve surrounding content).
   - After completing a module, present results and ask for confirmation to proceed to the next module.

- VSCode / Copilot specifics:
  - Do not auto-accept Copilot completions into the workspace. Treat Copilot suggestions as advisory diffs only.
  - For edits in VSCode, follow the Safe-Edit Protocol: Read → Think (anchor) → Act.
  - Prefer non-destructive, reversible VSCode-friendly commands (git-aware, small commits).

## Core constraints & preferences
- Strict: Do NOT use nodejs. If server-side behavior is required, propose a client-side alternative or explain the conflict.
- Preference: Keep solutions simple — HTML/CSS/Vanilla JS first (Minimum Viable Simplicity).
- Copilot-specific: In Code Shield-2, Copilot suggestions are advisory; never accept or commit suggestions without following the Safe-Edit Protocol and any required approvals.

## Contribution & workflow hints
- Keep changes small and module-scoped to simplify review.
- Use the product roadmap template (product_roadmap.md) to structure feature breakdown and priorities.
- When unsure of repository layout, list files before edits.
- Use clear commit messages that reference the module being implemented.

## Quick comparison between editions

- Code Shield-1 (Gemini edition)
  - Core: Gemini-focused agent that uses `gemini code cli`.
  - Emphasis: strict Module-Driven Engineering (MDE), Safe-Edit Protocol, English-only research.
  - Constraints: no nodejs; prefer HTML/CSS/Vanilla JS.
  - Use: intended for workflows that rely on Gemini tooling and CLI commands.

- Code Shield-2 (VSCode Copilot edition)
  - Core: same MDE and Safe-Edit rules adapted for Visual Studio Code + GitHub Copilot.
  - Extra rules: treat Copilot suggestions as advisory; never auto-accept suggestions without following Safe-Edit and approvals.
  - VSCode guidance: prefer safe, reversible VSCode CLI/workspace actions and small, module-scoped commits.

- Arabic edition
  - Core: Arabic translation of the Gemini protocol that preserves all rules and mandatory steps.
  - Use: for Arabic-speaking collaborators who must follow identical MDE and approval flows.

- Commonalities
  - All editions: Foundation-first phase, mandatory roadmap approval, per-file Safe-Edit Protocol, Jakob’s Law for UI/UX, no nodejs requirement, simple client-first stack (MVS).
  - Roadmap template, research requirements, and module loop are consistent across editions.

## License
This project is licensed under the Apache License 2.0 — see the LICENSE file for details.