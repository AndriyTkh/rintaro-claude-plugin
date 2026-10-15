# Suggestions in the Inbox (review queue)

Tools: `list_review_items`, `resolve_review_item`, `suggest_links`, `suggest_metadata`, `set_file_meta`,
`list_plans`, `get_plan`.

The Inbox holds suggestions next to notifications: links between files and tasks, document metadata, plans
waiting for a look, and conflicts between documents. Rintaro's link check adds link suggestions after every
upload; you add yours with `suggest_links` and `suggest_metadata`. Each item is the person's own and names
only what they can see.

1. When the person asked for the change ("link these", "this is the signed contract"), do it directly:
   `link_files`, `set_file_meta`. Suggest instead only when you are unsure or it is your own idea.
2. A suggestion says why in a few words ("both mention D2.3") and where it was read ("page 3"). Confidence:
   0.7 and up shows as likely.
3. Metadata: document type in the workspace's own words, the date the document speaks for, valid until,
   authority (1 signed agreement or legal, 2 approved plan or budget, 3 technical spec, 4 meeting or Slack
   decision, 5 working document, 6 agent note), codes. Name where you read each field in `sources`.
4. To go through the Inbox with the person: `list_review_items`, read them out briefly, and on their answer
   `resolve_review_item` (accept, dismiss, snooze, done). Accepting makes the change as the person, one undoable
   step; `reopen` undoes it.
5. A plan the person applied in part or rejected in Rintaro: `get_plan` shows what was chosen and their comment;
   the comment also arrives in `agent_inbox_list`.
