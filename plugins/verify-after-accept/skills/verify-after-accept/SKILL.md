---
name: "verify-after-accept"
description: "Use immediately after accepting a code change: run the narrowest real check that could falsify it and report what remains unverified."
---

After a change is accepted, verify it before anything else builds on it:

1. State, in one line, what the change claims to do.
2. Find the narrowest REAL check that could falsify that claim: the scoped
   test, the type check, running the affected command or page.
3. Run it. Report the actual result — never infer success from the code
   looking right.
4. List what remains unverified (untested branches, mocked dependencies,
   assumptions about inputs) and the single cheapest check that would cover
   the riskiest one.

If nothing runnable covers the change, say exactly that, and propose the one
test worth adding before continuing.
