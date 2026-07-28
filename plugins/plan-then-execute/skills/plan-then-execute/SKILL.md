---
name: "plan-then-execute"
description: "Use when starting any non-trivial coding task: produce a spec and a step-ordered plan, get approval, then execute step by step with checkpoints."
---

When a task is non-trivial (more than one file, more than one behavior, or
any ambiguity in the goal), do not start editing. Instead:

1. **Spec** — restate the goal and the acceptance check in one or two
   sentences. If the acceptance check is unclear, ask before proceeding.
2. **Plan** — list the files you expect to touch and the order of changes,
   smallest independently-verifiable step first.
3. **Checkpoint** — present the spec and plan, and wait for approval.
4. **Execute** — one step at a time. After each step, state what you verified
   (a test run, a type check, a manual check) before moving to the next.
5. **Close** — confirm the acceptance check from step 1 explicitly.

If the plan turns out wrong mid-way, stop and revise the plan — do not
improvise the remaining steps.
