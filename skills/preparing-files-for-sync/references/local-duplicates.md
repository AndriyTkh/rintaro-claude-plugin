# Duplicate files on the computer

Tools: the local file tools. Duplicates already in Rintaro belong to the managing-rintaro-files skill.

1. Group files by size; only groups with more than one file are candidates. Hash those (SHA-256 or MD5) to confirm
   identical content. Leave files over 10 GB out and list them.
2. In each group keep one copy: the one in the most specific folder (deepest, or the one whose folder name fits
   the content), else the newest. Say why for each group.
3. Show the groups, the copy kept and the copies to move, plus the space saved. Wait for an explicit yes.
4. Log each move in `_Rintaro review/<date>/changes.csv`, then move the extra copies to
   `_Rintaro review/<date>/duplicates/`, keeping their relative paths.
