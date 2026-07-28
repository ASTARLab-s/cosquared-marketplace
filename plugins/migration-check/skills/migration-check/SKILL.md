---
name: "migration-check"
description: "Use on any database schema or migration change: check reversibility, defaults, nullability against existing rows, and that a test exercises the new shape."
---

For any schema or migration change, verify before it merges:

1. **Reversibility** — is there a down path, or is this explicitly one-way?
   State which, and what the rollback plan is if it ships broken.
2. **Existing rows** — do new NOT NULL columns have defaults or backfills?
   Would the migration lock a large table? Check against the real row shape,
   not the ORM model.
3. **Consumers** — which queries and endpoints read the changed shape? Flag
   any that would break mid-deploy (old code, new schema).
4. **Coverage** — point at the test that exercises the new shape. If none
   exists, draft it now; a migration without a test is unverified by
   definition.

Report each of the four with a pass / fail / not-applicable and one line of
evidence.
