# Awesome Cursor Rules 🥝

**Free, copy-paste rules that make AI coding agents write current, correct code.**
Cursor `.mdc` rules, `AGENTS.md` and `CLAUDE.md` templates for Next.js, React, TypeScript, Python, Node, Unity, Godot and more. MIT licensed.

AI agents are trained on years of old code, so they happily write Godot 3 syntax, Pydantic v1, Tailwind v3 config and `pages/` routes. These short, focused rules tell the agent what's current and how to behave: small diffs, real verification, no invented APIs.

## Contents

| Stack | Rule | What it fixes |
|---|---|---|
| General | [core-behaviour.mdc](rules/general/core-behaviour.mdc) | Small diffs, read before editing, verify before "done" |
| General | [security-basics.mdc](rules/general/security-basics.mdc) | Input validation, server-side auth, secrets hygiene |
| General | [git-commits.mdc](rules/general/git-commits.mdc) | Conventional Commits, no force-push, clean staging |
| Next.js | [nextjs-app-router.mdc](rules/nextjs/nextjs-app-router.mdc) | App Router, Server Components, async `params` (Next 15+) |
| React | [react-components.mdc](rules/react/react-components.mdc) | React 19 patterns, fewer pointless effects, a11y |
| React | [tailwind-v4.mdc](rules/react/tailwind-v4.mdc) | Tailwind v4 CSS-first config and v3 → v4 renames |
| TypeScript | [typescript-strict.mdc](rules/typescript/typescript-strict.mdc) | No `any`, zod at the edges, discriminated unions |
| Python | [python-modern.mdc](rules/python/python-modern.mdc) | Python 3.12+ typing, uv, ruff, pathlib |
| Python | [fastapi.mdc](rules/python/fastapi.mdc) | Pydantic v2, `Annotated` deps, `lifespan`, async correctness |
| Node API | [express-5.mdc](rules/node-api/express-5.mdc) | Express 5 async errors and new path syntax |
| Unity (C#) | [unity-6.mdc](rules/unity-csharp/unity-6.mdc) | Unity 6 renames (`linearVelocity`), Input System, perf |
| Godot | [godot-4-gdscript.mdc](rules/godot/godot-4-gdscript.mdc) | Godot 3 → 4 table, static typing, signals |
| Testing | [tests-first.mdc](rules/testing/tests-first.mdc) | Tests with every change; never weaken tests to pass |
| Template | [AGENTS.md](templates/AGENTS.md) | Fill-in-the-blanks project brief for any agent |
| Template | [CLAUDE.md](templates/CLAUDE.md) | Claude Code file that reuses AGENTS.md |

## How to install

### Cursor
1. Create `.cursor/rules/` in your project root.
2. Copy the `.mdc` files you want into it (keep the frontmatter).
3. `alwaysApply: true` rules load on every request; others attach automatically when you edit files matching `globs`, or when the agent decides the `description` is relevant.

```bash
mkdir -p .cursor/rules
curl -sL https://raw.githubusercontent.com/grizzlykiwidev/awesome-cursor-rules/main/rules/general/core-behaviour.mdc -o .cursor/rules/core-behaviour.mdc
```

### Claude Code
Copy [`templates/CLAUDE.md`](templates/CLAUDE.md) to your project root. Paste the body of any rule (without the `---` frontmatter) into `CLAUDE.md`, or keep rules in `AGENTS.md` and import it with `@AGENTS.md`.

### Codex, Copilot, Windsurf and other agents
Copy [`templates/AGENTS.md`](templates/AGENTS.md) to your project root, fill it in, and paste the bodies of the rules you want under a `## Rules` heading. Most modern agents read `AGENTS.md` automatically.

## Tips
- Fewer, sharper rules beat one giant file. Pick only the stacks you use.
- Explicit "old → new" tables work far better than "use the latest version".
- Put your real commands in `AGENTS.md`. Agents that can run tests write better code.

## Want more?
These rules are maintained by **[Grizzly Kiwi Dev](https://grizzlykiwidev.github.io/)**.
- 🆓 **[Agent Rules Starter (free)](https://grizzlykiwi.gumroad.com/l/rdubay)**: a ready-to-drop-in pack with a Next.js + Supabase rule, templates and 10 vibe-coding prompts.
- ⭐ **[Agent Rules Starter Pack](https://grizzlykiwi.gumroad.com/l/xgdajx)**: 12 tested rules across 9 stacks (incl. Unreal Engine 5), pre-filled AGENTS.md templates, 30 prompts and workflow guides.

Follow [@GrizzlyKiwidev](https://x.com/GrizzlyKiwidev) for new rules.

## Contributing
PRs welcome. See [CONTRIBUTING.md](CONTRIBUTING.md). Keep rules short, specific, current and tested on a real project.

## License
[MIT](LICENSE) © 2026 Grizzly Kiwi Dev
