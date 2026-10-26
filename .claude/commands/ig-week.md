---
description: Weekly Instagram workflow — analytics → plan → captions + reel scripts → your approval → scheduling
argument-hint: [optional notes, e.g. "market at Granville Island Sat"]
---
Run Salar's weekly Instagram workflow. Extra notes from Salar: $ARGUMENTS

Rule: nothing is published, scheduled or sent without Salar's explicit "yes". Keep every output short and scannable.

1. **Analytics** — use the `analytics-reporter` subagent for last week's results. If Metricool has no Instagram connected, note it and continue without data.
2. **Plan** — use the `content-strategist` subagent, passing the analytics summary and the notes above. Get a 3–5 item table.
3. **Content** — in parallel:
   - `caption-writer` subagent: captions for every item in the plan.
   - `reel-scripter` subagent: a script for every REEL in the plan.
4. **Approval** — show Salar everything in one compact view: the analytics summary (≤5 lines), the plan table, then per post its caption + script (if reel). Ask: "Which posts are approved? Reply with numbers, edits, or 'all'." Then STOP and wait. Apply any edits and re-show changed posts.
5. **Schedule (all networks)** — only for approved posts, and only once Salar has given media URLs: use the `distribution-manager` subagent to build the cross-posting plan (Instagram, TikTok, Facebook, YouTube Shorts at each network's peak time, with at least one Trial Reel/collab for new audiences). Show Salar the plan and STOP for his "yes". Then do the scheduling here in the main conversation following `.claude/agents/distribution-manager.md` section 4 — never schedule anything he hasn't said "yes" to.
6. Finish with a 3-line summary: what's scheduled (with times), what's waiting on media, what was skipped.
