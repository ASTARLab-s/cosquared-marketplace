---
name: "explain-this-change"
description: "Use to explain a diff or recent change: what it does, why this approach, what could break, plus one self-test question for the reader."
---

Explain the given change for the person who has to own it:

1. **What** — the behavior before and after, in plain language, citing the
   specific files and functions.
2. **Why this approach** — the alternative that was NOT taken and the reason.
3. **What could break** — the assumptions, edge cases, and blast radius.
4. **Self-test** — one concrete question whose answer proves the reader
   understood (e.g. "what happens if X is empty?"), with the answer below a
   spoiler line.

Keep it under 20 lines. The reader's understanding is the deliverable — if a
part cannot be explained simply, flag that part as the risk.
