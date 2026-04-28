# Obsidian setup (Agent)

## Purpose
- Provide a copy/paste prompt and key settings to replicate this vault layout.
- Keep agent-facing rules compact; point to canonicals for logging and security.

## Vault location
- Local vault root: `/path/to/your/vault` (replace)

## How this works?
- The AI only needs access to the vault folder to read/write; no separate API required.
- The `cloud.md` file at the root is a guide that tells the AI how the vault is structured and where to store data.

## Copy/paste prompt (share with others)
```
You are setting up Obsidian to match my layout. Use the following files as the source of truth:
- .obsidian/app.json
- .obsidian/appearance.json
- .obsidian/core-plugins.json
- .obsidian/community-plugins.json
- .obsidian/graph.json
- .obsidian/workspace.json
- .obsidian/workspaces.json

Steps:
1) Copy the files above into your vault’s `.obsidian/` folder.
2) Open Obsidian and reload the vault.
3) If you plan to share the copied files, clear saved search text and `lastOpenFiles` in `workspace.json`.
4) Verify core and community plugins match the list below.
5) Re-open Obsidian to confirm the layout loads with a collapsed right sidebar.
6) Update any path-based graph color groups to match your vault structure.
```

## Config files to copy
- `.obsidian/app.json`
- `.obsidian/appearance.json`
- `.obsidian/core-plugins.json`
- `.obsidian/graph.json`
- `.obsidian/workspace.json`
- `.obsidian/workspaces.json`

## Suggestion structure (template)
1. `Context` — strategy, team.
2. `Daily` — daily journal, decisions, timeline.
6. `Projects` — ongoing projects or clients.
7. `Resources` — prompt library, templates, frameworks.
8. `Skills` — reference material for AI automation tasks.
9. `Tasks` — to-do list.

## Enabled plugins
- Core: file explorer, global search, switcher, graph, backlinks, canvas, outgoing links, tag pane, properties, page preview, daily notes, templates, note composer, command palette, editor status, bookmarks, markdown importer, outline, word count, workspaces, file recovery, sync, bases.
- Community: `<list your community plugins here>`.

## Appearance defaults
- Accent color: `<hex>` (example: `#4bb8e7`)
- Translucency: `<true|false>`

## App defaults
- Prompt on delete: `<true|false>`

## Graph defaults
- Show tags: `<true|false>`
- Show attachments: `<true|false>`
- Show orphans: `<true|false>`
- Hide unresolved: `<true|false>`
- Show arrows: `<true|false>`
- Color groups (update to match your vault):
  - `tag:vault/root`
  - `path:Context`
  - `path:Daily`
  - `path:Projects/<project>`
  - `path:Resources`
  - `path:Skills`
  - `path:Tasks`

## Workspace layout (summary)
- Left sidebar: file explorer, search, bookmarks (width ~`<width>`).
- Right sidebar: backlinks, outgoing links, tags, all properties, outline, reminders (collapsed, width ~`<width>`).
- Main pane: single editor tab (or describe your tabs).

## Workspace hygiene
- Remove `search.query` and `lastOpenFiles` entries in `workspace.json` before sharing.
- Avoid copying any saved search text that could include sensitive strings.

## Agent navigation guide
- Use `cloud.md` in the vault root as the system prompt for navigation.
- Follow its folder map and scoped-reading rules before searching widely.
- When unsure where to write, add a short entry in `Daily/` and a task in `Tasks/`.

## Logging + security rules
- Follow vault rules in [[AGENTS]] and log changes via [[Daily/logs/Index]].
- Do not store secrets or tokens in notes or logs. Use placeholders and env vars only.
