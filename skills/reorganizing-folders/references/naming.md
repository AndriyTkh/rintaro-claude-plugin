# Renaming by convention

Tools: `get_workspace_guide`, `list_spaces`, `list_files`, `check_names`, `apply_changes`, `plan_changes`,
`apply_plan`.

1. Read the naming convention in the guide (for example "YYYY-MM project - topic"). No convention there: ask the
   person for one and offer `propose_guide_change` to record it.
2. List the folders or files in scope and the ones that do not match.
3. Propose a new name for each; keep the meaning, change only the form. Run the new names through `check_names`
   (with `folderId` for files, to catch clashes ignoring case).
4. The new names are your proposal: `plan_changes` with one `rename` per item, and show old and new names side by
   side; at most 200 per plan. If the person already gave the exact names, use `apply_changes` directly.
5. On their yes, `apply_plan`; it needs no second confirmation. Mention that links people saved still work (ids do not change), but local
   copies synced by hand may need the same rename.
