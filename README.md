# CoSquared Marketplace — Claude Code plugins

Validated skills and commands for AI-assisted development, from
[CoSquared](https://cosquared.astar.inc/marketplace).

## Install

```
/plugin marketplace add ASTARLab-s/cosquared-marketplace
```

Then install any plugin from the list with `/plugin`.

## What "validated" means

Every item passes an executable policy lint before it can be published — no
dynamic-context shell preprocessing, no network fetches in executable positions,
path-safe artifacts, spec-valid frontmatter, secret-scanned, and a review date
under 400 days old. The lint runs in CI as a merge gate, so the badge is a
program rather than a promise.

## Also available without Claude Code

```
cosq add <slug>
```

Works signed out, and supports Cursor and Codex artifact formats too.

---

Generated from the CoSquared catalog by `scripts/build-plugin-marketplace.ts`.
Do not edit by hand — changes belong in the catalog, where the policy lint runs.
