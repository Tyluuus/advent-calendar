---
name: review
description: Senior-level review of my uncommitted changes. Use when I type /review or ask for a code review before committing.
---

Review the current uncommitted diff (`git diff` and `git diff --staged`) as a senior backend engineer
would in a product company. Don't rewrite the code; explain and let me fix it.

Check, in this order, and only report what actually applies:
1. Correctness of business rules (assignment, unlocking, moderation) against CLAUDE.md.
2. Data: N+1 queries, missing indexes for the queries I wrote, missing constraints,
   transactions where two writes must succeed together, race conditions.
3. Security: auth/role checks, locked-day content leaking, input validation, secrets.
4. Error handling and HTTP status codes.
5. Tests: is the new rule covered by an integration test? What case is missing?
6. Readability and naming (brief).

Format: a short list, most important first. For each item: file:line, what's wrong,
why it matters in production, and a hint (not the full fix).
End with: "Can you explain <one specific part of this diff> out loud?" — pick the part
I'm most likely to have accepted without understanding.
