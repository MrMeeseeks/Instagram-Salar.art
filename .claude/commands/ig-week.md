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
5. **Schedule** — only for approved posts, and only once Salar has given media URLs: do the scheduling here in the main conversation following the rules in `.claude/agents/scheduler.md` (get best time, show the exact post + time, wait for "yes" for each post, then call Metricool createScheduledPost). Do not schedule anything without a "yes" to that exact preview.
6. Finish with a 3-line summary: what's scheduled (with times), what's waiting on media, what was skipped.
