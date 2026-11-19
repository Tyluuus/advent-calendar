---
name: wrap
description: Close a session and update PROGRESS.md. Use when I type /wrap or say I'm done for today.
---

1. Summarise this session from the diff, commits and our conversation.
2. Add an entry at the top of "Session log" in PROGRESS.md (today's date):
   Done / Learned (concepts, in my words where possible) / Decisions (+ why) /
   Open questions / Next (one concrete first step for next session).
3. Update "Current milestone", "Next step" and "Open decisions" if they changed.
   If a decision was made, also add a one-line entry to the Decisions log in CLAUDE.md.
4. Propose a conventional commit message for any uncommitted work. Don't commit
   without my confirmation.
5. Keep the whole entry under 15 lines. Future me reads this cold after a week off.
