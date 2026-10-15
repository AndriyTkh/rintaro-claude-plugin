# Filing an upload ("Organize with Claude")

Tools: `list_imports`, `get_import_report`, `get_workspace_guide`, `list_spaces`, `list_files`, `check_names`,
`apply_changes`, `plan_changes`, `apply_plan`, `discard_plan`, `suggest_links`, `set_file_meta`.

Typical case: someone uploaded a folder and wants its files where they belong ("Organize with Claude" on the upload
report sends them here). People upload into folders they can write; there is no import inbox.

1. Find the upload: `list_imports`, then `get_import_report` on it. It lists the files, names that need a person
   (with a suggestion), duplicate sets, scans waiting for text, and files not linked to a task yet.
2. Ask, in one message, unless the person already said:
   - which files: all of the upload, only those not filed yet, or chosen folders;
   - where you may file: only folders the person can add to (`list_spaces` shows their level);
   - what you may do: create folders, rename, move, link to tasks, set metadata, archive exact duplicates,
     create tasks;
   - anything else to know (a note).
3. Read the guide: the folder structure, naming rules and who should see what. Do not invent new top-level folders.
4. Check new names with `check_names` (pass the destination as `folderId` to catch clashes).
5. Build the changes: "move" for files and folders, "create_folder" for missing destinations (give each a `ref`
   and use it as `toFolderRef`), "rename", "link_file_task" (file `id`, `taskId`), "set_file_meta" (docType,
   docDate, authority, codes), "archive" only for exact duplicates (same content, listed in the report).
6. Destinations the person or the guide named: `apply_changes` directly. Your own choices: `plan_changes` with a
   `title`, the person's `request` in their words and your `summary`; it waits in their Inbox, where they can
   apply all or some of it, or reply. Show the plan's `reviewUrl`.
7. Links you are unsure of: `suggest_links` (they wait in the Inbox) instead of linking.
8. Report grouped by destination. Point out every item whose access changes: "after the move, Marketing
   can read it", "a named colleague loses access". Refused items: say why and what would fix it.
9. More than 200 changes or 20 GB: one batch per destination group. Leave the emptied folder; archive it only
   if the person asks.
