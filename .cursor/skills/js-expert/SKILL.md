---
name: js-expert
description: >-
  Applies senior JavaScript/TypeScript engineering judgment—modules, async,
  runtime semantics, Node and browser APIs, tooling, and frontend patterns. Use
  when writing or reviewing .js, .ts, .tsx, .mjs, or .cjs code, or when the user
  mentions JavaScript, TypeScript, Node, React, or frontend/backend JS.
---

# JavaScript / TypeScript expert

## Default stance

- Prefer **clear, maintainable** code; follow **project ESLint/Prettier/tsconfig** and existing patterns (CommonJS vs ESM, test runner) before generic style wars.
- **Read before changing**: `package.json`, `tsconfig`, path aliases, and how neighboring files import/export.

## Language semantics

- **Equality**: Prefer `===` / `!==` in JS unless the project consistently uses loose equality for a documented reason.
- **Async**: Use `async`/`await` or Promises consistently with the file; handle rejections (try/catch or `.catch()`); avoid floating promises in app entrypoints.
- **Types (TS)**: Prefer explicit **public** APIs and tricky unions; avoid `any` unless escaping a legacy boundary—narrow with guards.
- **Modules**: Respect **ESM vs CJS** interop (`import`/`require`, `default` vs namespace); match bundler/runtime (Node, Vite, Webpack) expectations.

## Runtimes

- **Browser**: mind CSP, CORS, and bundle size; avoid blocking the main thread for heavy work (workers or chunking when appropriate).
- **Node**: use appropriate APIs (`fs/promises`, `path`, streams); set timeouts on outbound HTTP; don’t block the event loop.

## React / UI (when applicable)

- Follow **hooks rules** and existing state approach (Context, Redux, etc.); stable keys in lists; avoid unnecessary effect deps churn—derive state when possible.

## Testing and tooling

- Use the repo’s test stack (**Vitest**, **Jest**, **Mocha**, etc.); mock at boundaries (HTTP, clock) as the project does.
- Run **lint/format/typecheck** commands from `package.json` after substantive edits.

## Security

- Sanitize or parameterize anything reaching **DOM** (`dangerouslySetInnerHTML` only when unavoidable and trusted); validate untrusted input at boundaries.

## When unsure

- Prefer **MDN**-aligned behavior and **TypeScript handbook** patterns, then **repository conventions** over blog trends.
