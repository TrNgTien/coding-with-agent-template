---
name: obsidian-vault-log
description: >-
  Ensures agents write Obsidian vault maintenance to the journal and Daily/logs
  themed changelogs, update Daily/logs/Index, and summarize edits in replies—
  without secrets or PII. Use when editing markdown in a knowledge vault, Daily
  notes, Projects docs, AGENTS files, or .obsidian config, or when the user
  asks for vault changelog discipline.
---

# Obsidian vault logging (agents)

## When this applies

Any time you **write or materially edit** files in an Obsidian/knowledge vault (especially one whose root `AGENTS.md` defines logging rules).

## Required actions (default)

1. **Journal** — `Daily/YYYY-MM-DD.md` at vault **Daily** root: under **Done**, add bullets describing the work and **`[[wikilinks]]`** to changed notes. Create the day file if missing. Use the correct calendar date.

2. **Themed changelog** — If the vault uses `Daily/logs/<theme>/`, add `YYYY-MM-DD[-slug].md` when the change matches a theme (structure, Obsidian UI, project documentation, security policy). Each file: title, bullets, wikilinks, trailing link to the logs index if the vault pattern includes it.

3. **Index** — New `Daily/logs/...` file → add wikilink under the vault’s `Daily/logs/Index.md` **Entries** list.

4. **Chat reply** — Short **Vault updates**: path → one-line description. No secret values or tokens in the reply.

## Content rules

- **Bullets**; English unless the vault says otherwise.
- **No secrets:** no API keys, passwords, session tokens, private keys, or raw PII in journal or `Daily/logs/` bodies.
- **Prefer links** over pasting long excerpts.

## If the vault’s AGENTS disagrees

Follow the **vault’s** root `AGENTS.md` and `Daily/logs/AGENTS.md` when they exist; this skill is the generic checklist.

## Skip only when

Truly **non-substantive** edits (e.g. one-character typo). Still mention saved paths in the reply if anything was written.
