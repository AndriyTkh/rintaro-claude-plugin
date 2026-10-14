# Filing an import folder

Tools: `get_workspace_guide`, `list_spaces`, `list_files`, `check_names`, `plan_changes`, `apply_plan`,
`discard_plan`.

Typical case: someone uploaded a folder ("Import" or a dated landing folder) and wants its files where they belong.

1. Read the guide: the folder structure, naming rules and who should see what.
2. `list_spaces` for the tree, `list_files` on the import folder and its subfolders.
3. Propose a destination per subfolder or group of files, following the guide. Where the guide does not say,
   ask; do not invent new top-level folders.
4. Check new names with `check_names` (pass the destination as `folderId` to catch clashes).
5. Call `plan_changes` with op "move" for files and folders and op "create_folder" for missing destinations (give each
   new folder a `ref` and use it as `toFolderRef`).
6. Show the plan grouped by destination. Point out every item whose access changes: "after the move, Marketing
   can read it", "a named colleague loses access". Refused items: say why and what would fix it.
7. Explicit yes, then `apply_plan`. More than 200 changes: one plan per destination group, a yes for each.
8. Leave the emptied import folder where it is; archive it only if the person asks, through another plan.
