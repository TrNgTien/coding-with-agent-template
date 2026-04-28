---
tags:
  - vault/root
---

# Obsidian — AI navigation map (template)

Local Markdown vault; grant AI filesystem access. Obsidian is optional UI.

## How it works
- **Save** into the folder that matches intent. If unclear: brief note in `Daily/` and a `Tasks/` item when something must be done.
- **Answer priorities / what to do:** `Tasks/`, recent `Daily/`, active `Projects/`.
- **Answer strategy / standards / process:** `Context/` first.

## Scoped reading (principle)
Not every question needs every note. Match context to the topic:
- **A specific day’s story** → that day’s daily note (`Daily/YYYY-MM-DD.md`) and the notes it links to.
- **A concrete task or project** → the relevant `Projects/...` page plus applicable `Context/` notes.
- **Agents** should prefer naming which files to open next over implying the whole vault must be loaded.

## Folder map (general)
| Folder | Purpose | Typical contents |
|--------|---------|------------------|
| **Context** | Durable org context | Strategy, team,policies |
| **Daily** | Continuity | Work log, decisions, blockers |
| **Projects** | Scoped work | Per project or client |
| **Resources** | Reuse | Commands, templates, prompts |
| **Skills** | Agent/task packs | Task references, procedures |
| **Tasks** | Action | Backlog, next up, priorities |

## Conventions
- **Language:** pick one default for new notes.
- **Wikilinks:** `[[Note name]]`.
- **Daily:** `Daily/YYYY-MM-DD.md` or one rolling file—pick one pattern.
- **Preferences** (e.g., “always run tests before commit”): keep in `Context/`; link from `Skills/` when automation needs them.

## Quick prompts
- *“Remember …”* → `Context/` or `Skills/`; reply with path.
- *“What should I focus on?”* → `Tasks/`, latest `Daily/`, `Projects/`.
- *“Where does X live?”* → `Context/` or `Projects/`.

---

*Vault changelog:* `Daily/logs/Index` · *Root pointer:* `Second Brain - Setup log`
