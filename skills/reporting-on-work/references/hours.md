# Hours

Tools: `get_timesheet`, `list_people`, `list_work_packages`, `search_tasks`.

1. `get_timesheet` gives a person's week; reading other people's sheets needs the hours-review permission, so the
   person may only see their own. Say so when others are missing.
2. Collect the weeks in the period, then sum by person, work package (through each task's work package) and month.
3. Show a table with totals, and the weeks that are still open or returned (not yet approved), since their hours
   may still change.
4. Change nothing; corrections go through the timesheet workflow of the planning skill.
