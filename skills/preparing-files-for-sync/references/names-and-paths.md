# Names and paths

Tools: the local file tools, `check_names`.

1. Send the relative paths to `check_names` with `paths` true (up to 5,000 per call). For each failing entry it
   gives the problems and the `fixed` path: the name Rintaro would store anyway.
2. Use the fixed name unless the person prefers another; run any name they choose through `check_names` again.
   Two names that differ only in case in one folder cannot both exist in Rintaro: the second gets " (2)".
3. Paths over 240 characters: propose shorter folder names near the top of the path (one rename fixes many
   paths). Never truncate file names silently.
4. Show an old-to-new table and wait for an explicit yes, at most 200 renames per batch.
5. Log every rename in `_Rintaro review/<date>/changes.csv` before doing it, rename deepest items first, and check
   that the new paths exist.
