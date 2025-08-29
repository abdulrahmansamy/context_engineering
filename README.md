# Context Engineering for AI Coding

Context Engineering repository: protocol documents and templates for iterative, module-driven app construction by an AI-assisted engineer.

## What this repo is
A small collection of protocol documents, templates, and examples that define how an AI engineer (e.g., Code Shield / Cipher Gear / Cog Code ) should operate when building applications one functional unit at a time, with mandatory user verification.

<!-- Inspired by -->
**Inspired by:** https://github.com/Pythonation/Context-Engineering-for-AI-Coding/blob/main/README.md

## What problem does this protocol solve?
Are you fed up with the chaos of AI coding assistants? Does your helper build a brilliant feature in one step only to break it in the next? Do you feel like you're shouting instructions into the void and getting inconsistent, unmaintainable results?

This protocol targets that exact problem — the productivity-killing disorder of modern "Vibe Coding." The issue isn't simply that models need better prompts; it's that our interaction model is ad hoc. The protocol enforces a deterministic, module-driven workflow with mandatory user verification, safe per-file edits, and repeatable research and roadmap steps so AI contributions are consistent, reviewable, and maintainable.

## Solution — from "Prompter" to "Context Engineer"
This protocol isn't just a better system prompt. It's an operating model that turns an AI assistant from a creative-but-chaotic helper into a systematic software engineer. Instead of iterating by ad hoc instructions, you define identity, rules, and a repeatable workflow (context engineering) so the assistant behaves like an accountable engineer architect and builder.

## How it works (short)
- Identity: Give the assistant a fixed role (e.g., "Code Shield-1") so its behavior is constrained by purpose.
- Five core laws (summary):
  1. Foundation First — produce a product roadmap and obtain approval before writing code.
  2. Module-Based Loop — build one functional unit at a time, with user checkpoints.
  3. Mandatory Safe-Edit — Read → Think (anchor) → Act for every modified file.
  4. Tool-Aware Context — inspect the workspace when unsure (ls / ReadFolder).
  5. Intuition-First (Jakob’s Law) — prefer familiar UI patterns and minimal surprises.
- Phases:
  - Phase 1: Foundation & Verification — research (fact + inspiration), produce roadmap, wait for approval.
  - Phase 2: Module Construction — repeat: Think → Act (safe edits) → Verify, per module.

## How to use
1. Download the protocol markdown files from this repo and place them in your project's root:
   - Gemini_context/product_roadmap.md (roadmap template)
   - Gemini_context/Gemini_context-en.md (Code Shield-1 / Gemini protocol)
   - Gemini_context/Gemini_context-ar.md (Arabic protocol) <!-- ...keep Arabic path if present in repo... -->
   - vscode_Copilot_context/Copilot_context.md (VSCode / Copilot edition)
2. Open your preferred AI coding assistant that supports contextual files (Gemini Code CLI, Cursor, Phind, Claude, Copilot workflows).
3. Ask the assistant to follow the protocol and provide your project brief (e.g., "Create a task manager web app using flowmodoro").
4. Approve the roadmap when presented, then review each module after the assistant completes the Think→Act→Verify cycle.

## Key files
- vscode_Copilot_context/Copilot_context.md — Code Shield-2 (VSCode Copilot Edition) protocol (safe-edit rules, Copilot guidance).
- Gemini_context/Gemini_context-en.md — Code Shield-1 protocol (Gemini edition).
- Gemini_context/Gemini_context-ar.md — Arabic version of the protocol. <!-- keep if file exists -->
- Gemini_context/product_roadmap.md — Product roadmap template to be used in Phase 1.
- LICENSE — Apache License 2.0.

## Quick usage
1. Phase 1 — Foundation & Verification
   - User and agent draft research, fact & inspiration searches (English-only).
   - Agent prepares the Product Roadmap using the provided template (Gemini_context/product_roadmap.md).
   - Mandatory stop: the agent must request and wait for explicit user approval before writing any files.

2. Phase 2 — Module Construction
   - For each module in the approved roadmap:
     - User and agent review the module's requirements and success criteria.
     - Agent writes code, following safe-edit rules and module-driven workflow defined in Gemini_context/Gemini_context-en.md.
     - Mandatory checkpoint: user reviews and approves the module completion.

## Contribution & workflow hints
- Keep changes small and module-scoped to simplify review.
- Use the product roadmap template (Gemini_context/product_roadmap.md) to structure feature breakdown and priorities.
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