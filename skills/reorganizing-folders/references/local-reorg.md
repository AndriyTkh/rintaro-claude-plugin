# Reorganising a folder on the person's computer

Works only where Claude can reach the person's files (Claude Code, or Cowork with the folder granted). In a chat
without file access, say so and stop.

Tools: the local file tools, plus `get_workspace_guide` and `list_spaces` to align with Rintaro.

1. Work only inside the folder the person named. Skip system, program and hidden folders, online-only
   placeholders, and files that are open or locked. No moves to another drive.
2. List the current structure (folders, counts, sizes). Stop and ask after 200,000 files.
3. Propose the new structure; where the folder will go to Rintaro, mirror the Rintaro folders from the guide and
   `list_spaces` so a later upload lands cleanly.
4. Before moving anything, write `_Rintaro review/<date>/changes.csv` inside the folder: one row per move or
   rename with old path and new path. Show the person the counts and the first rows.
5. On an explicit yes, move in batches of at most 200 items; after each batch check that every new path exists.
6. Nothing is deleted. Things the person wants gone go to `_Rintaro review/<date>/`.
7. Undo: the person (or you) moves each row of `changes.csv` back, newest first.
