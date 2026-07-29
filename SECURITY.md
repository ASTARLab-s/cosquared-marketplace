# Security

## Reporting

Report anything that looks unsafe in a published plugin to **admin@astar.inc**.
Please do not open a public issue for a suspected supply-chain problem — mail
first so it can be pulled before it spreads.

## What is checked before an item is published

Every item passes an executable policy lint, run in CI as a merge gate:

- **No dynamic-context shell preprocessing.** The `!` backtick form that
  executes a command while a prompt is being assembled is rejected outright — it
  is the signature of the ToxicSkills class of attacks.
- **No network fetches in executable positions.** A fenced block may not
  `curl`/`wget` and pipe to a shell.
- **Path-safe artifacts only.** No absolute paths, no `..` traversal.
- **Secret scan** over every artifact, using the same redaction ruleset the
  CoSquared collector uses.
- **Spec-valid frontmatter**, verified to parse as YAML.
- **Review freshness** — an item older than 400 days without review fails.

Each rule has a negative fixture proving it fires.

## What this does NOT guarantee

These are instructions for a model, not sandboxed code. A skill can still ask
Claude to run commands, and you should read anything before installing it —
here or anywhere else. Every artifact in this repo is plain text and reviewable
in the diff.
