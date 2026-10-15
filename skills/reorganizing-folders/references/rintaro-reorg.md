# Reorganising folders in Rintaro

Tools: `get_workspace_guide`, `workspace_map`, `get_brief`, `list_spaces`, `get_space_access`, `check_names`,
`update_space`, `apply_changes`, `plan_changes`, `apply_plan`, `discard_plan`, `undo_change`, `submit_brief`,
`propose_guide_change`.

1. `workspace_map` (or `list_spaces`) gives the folders the person can read, with paths and their level. Moving or
   renaming a folder needs manage on it (and on the new parent); folders the person cannot manage come back refused.
2. Draw the current tree of the part in question and the proposed tree. Keep what the guide prescribes; ask
   before inventing new top-level folders.
3. Express the difference as changes:
   - op "create_folder" for new folders (give each a `ref`; later changes use it as `toFolderRef`);
   - `move` with `kind` folder and `toFolderId`, `toFolderRef` or `toTopLevel`;
   - `rename` with the new name (check names first with `check_names`, kind folder);
   - merging A into B: move A's subfolders and files into B, then `archive` the empty A.
4. The person asked for exactly this: call `apply_changes` (one folder move alone: `update_space` with
   the new parent or to the top level). It is the approval; do not ask again. More than 200 changes or 20 GB: batches.
5. Your own proposal, an unclear request, or the person wants to see it first: call `plan_changes`, show the new
   tree, the changes grouped by kind and the access changes, people by name; on their yes `apply_plan` (refused
   because something changed since: make a new plan and show it again); on no `discard_plan`.
6. Read the result either way:
   - `refused` items: explain the reason in plain words and what would fix it;
   - `access`: for every moved folder, who gained or lost sight of it, and `subfoldersChanged`;
   - moving a folder out of a Restricted folder needs manage on the Restricted folder; say who can do it.
7. Leave a `submit_brief` on the reorganised folder, offer `propose_guide_change` when the structure changed for
   good, and end with the activity id for undo.
