# Restructuring the task tree

Tools: `search_tasks`, `get_task`, `list_subtasks`, `list_work_packages`, `plan_changes`, `apply_plan`.

1. Find the tasks in question with `search_tasks` (and `list_subtasks` for a task's children).
2. Propose the target: another work package (`wpId`), under another task (`parentId`), or back to the top level
   (`clear` with "parent"). A task's subtasks move with it; its code stays.
3. Several tasks: one `plan_changes` with an op "edit_task" change per task. Status, priority, start and due dates
   can be set in the same plan. Assigning people is not part of a plan: use `assign_task` separately and name the
   person.
4. The plan shows when a task in a "space" visibility moves to a work package in another folder, and who gains or
   loses sight of it. Show that.
5. Explicit yes, then `apply_plan`. Refused items (no rights, a loop under its own subtask) are listed with why.
