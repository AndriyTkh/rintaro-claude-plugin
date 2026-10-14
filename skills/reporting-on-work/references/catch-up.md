# Catching up since a date

Tools: `my_notifications`, `list_activity`, `my_work`, `work_summary`, `mark_notifications_read`.

1. The date: what the person said ("since Friday"), else their last working day.
2. `my_notifications` (unread first) and `list_activity` with `since`, all pages. `actor` "me" shows what the person
   and their agents changed; entries with `viaAgent` were made by an agent for someone, so say so.
3. `my_work` for what is theirs now and `work_summary` with scope "me" from that date.
4. Write what matters to the person first: new or changed tasks of theirs, mentions, proposals waiting, deadlines
   that moved. Then the rest in a few lines. Change nothing, except: if the person asks, mark the notifications
   you showed as read with `mark_notifications_read` (their ids).
