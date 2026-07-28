---
name: "context-primer"
description: "Use to audit and refresh the project-instructions file: find stale commands, missing conventions, and undocumented gotchas, then draft the minimal update."
---

Audit the project's agent-instructions file against the repo as it is now:

1. Verify every stated command (build, test, lint, run) still exists in the
   project's manifests — flag the stale ones with their current replacement.
2. Compare stated conventions against the three most recently changed source
   files — note conventions the code follows that the file omits.
3. Check the gotchas section against recent debugging pain: anything a
   newcomer would still trip on that is not written down?
4. Draft the MINIMAL edit: corrections and the top missing items only. The
   file's value is density — do not pad it.

Present the draft as a diff for approval; do not rewrite the file wholesale.
