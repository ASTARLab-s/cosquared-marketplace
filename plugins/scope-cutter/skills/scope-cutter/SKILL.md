---
name: "scope-cutter"
description: "Use when a task is growing beyond one session: split it into the smallest landable slice and an explicit deferred list."
---

When the current task is growing past what this session can land:

1. Restate the user-visible outcome the task exists for.
2. Identify the SMALLEST slice that delivers a real piece of that outcome and
   can be verified and committed today.
3. Move everything else to an explicit "deferred" list with one line each on
   why it can wait. Deferred is a decision, not a leak.
4. Confirm the slice still passes its tests standing alone — no half-wired
   imports, no dead flags.
5. Finish the slice through to a commit before opening any deferred item.

Never grow the slice mid-way: if something deferred turns out to be required,
stop and re-plan rather than absorbing it silently.
