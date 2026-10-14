# Reorganising folders in Rintaro

Tools: `get_workspace_guide`, `list_spaces`, `get_space_access`, `check_names`, `plan_changes`, `apply_plan`,
`discard_plan`, `undo_change`, `propose_guide_change`.

1. `list_spaces` gives the folders the person can read, with paths and their level. Moving or renaming a folder
   needs manage on it (and on the new parent); folders the person cannot manage come back refused in the plan.
2. Draw the current tree of the part in question and the proposed tree. Keep what the guide prescribes; ask
   before inventing new top-level folders.
3. Express the difference as changes:
   - op "create_folder" for new folders (give each a `ref`; later changes use it as `toFolderRef`);
   - `move` with `kind` folder and `toFolderId`, `toFolderRef` or `toTopLevel`;
   - `rename` with the new name (check names first with `check_names`, kind folder);
   - merging A into B: move A's subfolders and files into B, then `archive` the empty A.
4. Call `plan_changes`. Read the result before showing it:
   - `refused` items: explain the reason in plain words and what would fix it;
   - `access`: for every moved folder, who gains or loses sight of it, and `subfoldersChanged`;
   - moving a folder out of a Restricted folder needs manage on the Restricted folder; say who can do it.
5. Show the plan: the new tree, then the changes grouped by kind, then the access changes, people by name.
6. On an explicit yes: `apply_plan`. If it is refused because something changed since, make a new plan and show
   it again. On no: `discard_plan`.
7. Offer `propose_guide_change` when the structure changed for good. End with the activity id for undo.
