---
name: follow-up
description: Draft a follow-up message to a Zoye contact or deal from its real history, and send it from Zoye only after the user approves. Use when the user asks to follow up, nudge, check in, or write to a lead or customer, by email or WhatsApp.
---

# Follow-up from Zoye

Follow the working-with-zoye rules.

1. Find the contact or deal with `query_records` and read the context with `get_full_context` (or `get_record` plus `get_recent_activity`): last messages, meetings, open tasks, stage.
2. Draft one short message that refers to something real from that history (the last meeting, the open question, the proposal sent). Match the language and tone of earlier messages. No invented facts, prices or promises.
3. Show the draft and ask the user which channel to use when it is not clear.

Sending:

- Find the send tool with `find_capability` ("send email" or "send WhatsApp message") and `describe_tool`, then call it through `execute_write` without `confirm` to get the preview.
- Show the preview and send only after a clear yes, with the returned `confirm_token`.
- WhatsApp outside the 24 hour reply window needs an approved template: if the preview says so, tell the user instead of forcing it.

After sending, offer to create a task for the next touch point, and create it only on a yes.
