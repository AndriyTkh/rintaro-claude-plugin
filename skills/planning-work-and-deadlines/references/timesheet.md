# Logging hours

Tools: `get_timesheet`, `search_tasks`, `log_hours`, `set_time_note`, `timesheet_action`.

1. `get_timesheet` for the week in question: what is logged, and whether the week is open.
2. Turn the person's words ("Monday 3 hours on the filter tests") into entries: day, task (find it with
   `search_tasks`), hours, optional note. Unclear task: ask.
3. Show the entries as a table and wait for a yes, then `log_hours` (and `set_time_note`) per entry.
4. Submit the week with `timesheet_action` only when the person says "submit". A submitted or approved week is
   locked; to change it they withdraw it first.
