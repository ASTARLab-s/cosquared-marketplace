# CoSquared Marketplace — Claude Code plugins

13 validated skills and commands for AI-assisted development, from
[CoSquared](https://cosquared.astar.inc/marketplace) — a privacy-first coach for
how you work with AI coding tools.

## Install

```
/plugin marketplace add ASTARLab-s/cosquared-marketplace
```

Then install any plugin below with `/plugin`.

## Plugins

| Plugin | What it does |
| --- | --- |
| [`ai-native-automation-leverage`](./plugins/ai-native-automation-leverage) | An /automate slash command (rule form for Cursor/Codex) that reviews each session for repeated manual work and proposes the smallest useful skill, command, or subagent to own it. For builders who want each session to compound. |
| [`backend-api-contract`](./plugins/backend-api-contract) | A verification subagent (rule form for Cursor/Codex) that runs your integration and contract tests after any route, schema, or migration change — and checks that request/response shapes still match their consumers. |
| [`tester-subagent`](./plugins/tester-subagent) | A Tester subagent for Claude Code (rule form for Cursor/Codex) that runs the project's test suite after accepted changes and reports honestly on what it could not verify. |
| [`explain-before-accept`](./plugins/explain-before-accept) | An /explain slash command (rule form for Cursor/Codex): what the change does, why this approach, what could break, and the one thing to verify yourself — before you accept it. |
| [`finish-the-thread`](./plugins/finish-the-thread) | A /wrap-up slash command (rule form for Cursor/Codex) that closes each session cleanly: summarize, confirm tests, draft the commit, and flag half-done work that should not land yet. |
| [`plan-then-execute`](./plugins/plan-then-execute) | A skill your agent invokes when a task is non-trivial: write the spec and acceptance check, produce a step-ordered plan, get it approved, then execute one step at a time with a checkpoint after each. The procedure form of the plan-first rule. |
| [`verify-after-accept`](./plugins/verify-after-accept) | A skill that runs after you accept a change: it re-derives what the change claims to do, runs the narrowest real check that could falsify it, and reports what remains unverified — so acceptance and verification stop drifting apart. |
| [`edge-case-hunter`](./plugins/edge-case-hunter) | A skill that inspects a change and its tests, enumerates the boundary conditions the tests do not cover — empty inputs, nulls, ordering, concurrency, unicode, limits — and drafts the two highest-value missing tests. |
| [`explain-this-change`](./plugins/explain-this-change) | A skill that turns any diff into a structured explanation: what changed, why this approach, what could break, and one question to test your own understanding — so comprehension keeps pace with acceptance. |
| [`scope-cutter`](./plugins/scope-cutter) | A skill that takes a ballooning task and splits it into the smallest landable slice plus an explicit later-list — so sessions end in commits instead of half-finished threads. |
| [`context-primer`](./plugins/context-primer) | A skill that audits your project-instructions file (CLAUDE.md / AGENTS.md / rules) against the repo as it exists today: stale commands, missing conventions, gotchas discovered since — and drafts the minimal update. |
| [`migration-check`](./plugins/migration-check) | A backend skill invoked on any schema or migration change: confirms reversibility or an explicit one-way call, checks defaults and nullability against live-row reality, and verifies a test exercises the new shape before it ships. |
| [`study-recap`](./plugins/study-recap) | A student skill that closes a working session by turning what was built into understanding: the concepts used, one re-implementation exercise, and the question you should be able to answer cold tomorrow. |

## What "validated" means

Every item passes an executable policy lint before it can be published — no
dynamic-context shell preprocessing, no network fetches in executable positions,
path-safe artifacts, YAML-valid frontmatter, secret-scanned, and a review date
under 400 days old. Each rule has a negative fixture proving it fires, and the
lint runs in CI as a merge gate — so the badge is a program, not a promise.

It is not a sandbox. See [SECURITY.md](./SECURITY.md) for what that does and
does not cover, and read anything before you install it.

## Also available without Claude Code

```
cosq add <slug>
```

Works signed out, and emits Cursor and Codex artifact formats too.

## Support

Questions, bugs, or anything unsafe: **admin@astar.inc**.
Security reports: see [SECURITY.md](./SECURITY.md) — please mail first.

## License

[Apache-2.0](./LICENSE). Install, fork, and adapt these freely.

---

Generated from the CoSquared catalog by `pnpm marketplace:plugins`.
Do not edit by hand — changes belong in the catalog, where the policy lint runs.
