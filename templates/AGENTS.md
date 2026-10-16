# AGENTS.md

> Instructions for AI coding agents (Cursor, Codex, Copilot, Claude Code via @AGENTS.md, and others).
> Keep this short and specific. Replace everything in <angle brackets>.

## Project
<One or two sentences: what this app does and who it's for.>

## Stack
- <e.g. Next.js 15 App Router, TypeScript, Tailwind v4, Supabase, Vitest>
- Package manager: <pnpm | npm | bun | uv>

## Commands
- Install: `<pnpm install>`
- Dev: `<pnpm dev>`
- Typecheck: `<pnpm typecheck>`
- Lint: `<pnpm lint>`
- Test: `<pnpm test>`

Run typecheck, lint and tests before saying a task is done.

## Layout
- `<src/app/>`: routes
- `<src/components/>`: UI components
- `<src/lib/>`: shared logic and clients

## Conventions
- Smallest change that solves the task; match existing style.
- No new dependencies without asking.
- Secrets only in env vars; update `.env.example`.

## Don't
- Don't edit generated files: <e.g. `src/types/database.ts`, migrations already applied>.
- Don't run destructive commands or force-push.
