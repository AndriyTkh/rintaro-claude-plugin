# Getting something back

Tools: `list_archive`, `list_files`, `restore_item`, `list_activity`, `undo_change`.

"Deleted" in Rintaro means archived: it stays restorable until the Owner purges the archive.

1. Folders, tasks and work packages: `list_archive` (filter by `kind` or the folder it sat in). Files: `list_files`
   with `archived` on the folder they were in.
2. Several matches: show name, where it was, when and by whom it was archived; ask which.
3. Restore:
   - a folder or task: `restore_item`; if its old folder is archived too, ask where to put it (`spaceId`);
   - a file: find the entry that archived it with `list_activity` (entity type file, or the plan that did it)
     and use `undo_change` on that entry; if that is refused because of later changes, the web app's archive
     view restores it;
   - a whole plan: `undo_change` with the plan's activity id.
   Restoring changes nothing else, so one yes is enough.
4. Not in the archive: it may have been purged by the Owner, or never shared with the person. Say both
   possibilities plainly and suggest asking the Owner.
5. End with where it is now.
