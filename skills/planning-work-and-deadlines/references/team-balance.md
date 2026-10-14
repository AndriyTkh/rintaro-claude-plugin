# Balancing the team's load

Tools: `workload`, `search_tasks`, `list_people`, `assign_task`.

1. `workload` for the weeks in question: each person's planned hours against capacity.
2. Find what makes the overloaded people overloaded (`search_tasks` by assignee and dates).
3. Suggest moves: later dates, or the same task proposed to someone with room. Each suggestion names both people.
4. Nothing is reassigned by you directly: on a yes, `assign_task` proposes the task to the new person, who accepts
   or declines. Dates move only with the assignee's or the lead's yes.
