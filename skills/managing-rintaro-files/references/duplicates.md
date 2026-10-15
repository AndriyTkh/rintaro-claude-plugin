# Duplicate files in Rintaro

Tools: `find_duplicates`, `get_file`, `plan_changes`, `apply_plan`.

Duplicates on the person's own computer belong to the preparing-files-for-sync skill, not here.

1. Call `find_duplicates` (whole workspace or one folder). A group is files with the same size and checksum.
2. For each group propose which copy to keep: the one with comments, then the one with most versions, then the
   one in the most specific folder that the guide names for it. Say why.
3. The others are archived, never deleted: `plan_changes` with `archive` for each extra copy.
4. Show the plan: per group the kept copy and the copies to archive, with their folder paths; and the space saved.
   Copies in folders other people use: name the folder and ask whether its people expect the file there.
5. Which copy stays is your proposal, so wait for their answer, then `apply_plan` (no second confirmation). Archived copies can be restored with `restore_item` or the plan's undo.
