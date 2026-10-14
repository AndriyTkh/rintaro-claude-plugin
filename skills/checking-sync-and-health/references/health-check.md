# Workspace health check

Tools: `health_report`, `get_task`, `workload`, `update_task`, `assign_task`, `plan_changes`, `apply_plan`.
The prompt `health_check` holds the same steps for clients without this skill.

1. Call `health_report` with scope "team" (or "me" when the person asks about their own work, or `spaceId` for
   one folder). The rules (overdue, at risk, no assignee, no due date, proposals waiting too long, overloaded
   people, empty work packages and more) live in the server; do not invent others.
2. Show the findings as the report orders them, most severe first: the title, the count, up to five examples
   (code, title, who, date) and the suggested fix in plain words. Nothing to fix: say so in one line.
3. Offer fixes one finding at a time:
   - one task: the exact field change, then `update_task` on a yes;
   - several tasks (for example new due dates for ten overdue tasks): one `plan_changes` with an op "edit_task" change per
     task, shown as a table, then `apply_plan` on a yes;
   - an assignee: `assign_task` per task, naming the person, after a yes.
4. Overloaded people: show `workload` and suggest moving or proposing work; never reassign without a yes.
5. End with the fixes applied, the activity ids, and what is left.
