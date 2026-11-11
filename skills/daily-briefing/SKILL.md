---
name: daily-briefing
description: A short start-of-day briefing from Zoye - meetings today, tasks due or overdue, deals that need a move, and new leads. Use when the user asks what is on today, for a morning summary, "what should I focus on", or a briefing from Zoye.
---

# Daily briefing from Zoye

Follow the working-with-zoye rules. This flow only reads; it changes nothing.

1. Call `get_briefing` for today. If the user named a workspace or a day, pass it.
2. If the briefing leaves gaps, fill them with `query_records`: tasks due today or overdue that are assigned to the user, events today, and deals with no activity for 14 days or more. Read the schema first for the right field and stage names.
3. Call `get_recent_activity` for what changed since yesterday (new leads, replies, stage moves).

Write it for a phone screen, in this order, and skip any empty section:

- **Today:** meetings with time, who, and the related deal or contact.
- **Due:** tasks due today, then overdue ones, oldest first.
- **Needs a move:** at most 5 deals that went quiet or have a close date this week, each with one suggested next step.
- **New:** leads and replies since yesterday.

End with one line naming the single most important thing to do first. Offer to create tasks or draft follow-ups, and do either only when the user says yes.
