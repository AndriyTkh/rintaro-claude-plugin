# Where the folders go in Rintaro

Tools: `get_workspace_guide`, `list_spaces`, `get_space_access`, `create_space`.

1. Read the guide (structure, naming, who sees what) and `list_spaces` (the folders the person can see).
2. For each top-level local folder propose a Rintaro destination. Default when unsure: a landing folder named
   "Import - <date>" that only the person (and the Owner) can see, so nothing is shared by accident; files are
   sorted from there later (managing-rintaro-files, filing imports).
3. For each destination say who will see the files there: `get_space_access` explains it for folders the person
   manages; otherwise say that the folder's people will see them.
4. Missing destination folders: list them; create them with `create_space` only after an explicit yes, one by one,
   and keep the activity ids for undo.
5. Offer to do the upload from here with the upload tools (the upload workflow in SKILL.md), or the person can use the Rintaro web app (Files, Upload folder); Rintaro Sync comes later.
