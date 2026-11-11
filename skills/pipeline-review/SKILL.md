---
name: pipeline-review
description: Review the Zoye deal pipeline - totals per stage, stuck or slipping deals, missing next steps - and propose stage moves and tasks. Use when the user asks about their pipeline, forecast, deals by stage, which deals are stuck, or wants a weekly sales review.
---

# Pipeline review

Follow the working-with-zoye rules.

1. Call `get_entity_schema` for deals to learn the pipelines, stage names, amount and close date fields of this workspace.
2. Pull open deals with `query_records`. For totals and trends prefer `run_report` or `run_analysis` over adding numbers up yourself.
3. Flag, per deal:
   - no activity in 14 days or more (`get_recent_activity` or the record's last activity date);
   - a close date in the past or within 7 days;
   - no open task, so no next step;
   - no amount or no contact linked.

Report:

- A table: stage, number of deals, total amount.
- Up to 10 flagged deals, worst first, each with the reason and one concrete next step.
- Proposed changes as a list: stage moves (`move_to_stage`), new tasks (`create_records`), missing links (`link_records`).

Make no change until the user approves the list, or the part of it they pick. Then apply exactly that, and say what changed.
