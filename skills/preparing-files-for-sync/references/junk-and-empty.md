# Junk, temp and empty items

Tools: the local file tools.

1. Candidates: Office lock files (`~$*`), `*.tmp`, `.~lock*`, `Thumbs.db`, `desktop.ini`, `.DS_Store`, zero-byte
   files, and folders that are empty after that.
2. Skip anything open or locked, and anything modified in the last hour (it may be in use).
3. Show the list with counts per kind and wait for an explicit yes.
4. Log each move in `_Rintaro review/<date>/changes.csv`, then move the items to `_Rintaro review/<date>/junk/`,
   keeping their relative paths. Empty folders are moved the same way, deepest first.
5. Nothing is deleted. Tell the person they can empty the review folder themselves once they are sure.
