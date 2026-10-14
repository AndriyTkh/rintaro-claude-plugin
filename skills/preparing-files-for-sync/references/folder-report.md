# Folder report

Tools: the local file tools, `check_names`.

1. Walk the folder (bounds and limits from the skill's safety block). Do not open file contents.
2. Count per top-level subfolder: files, total size, newest and oldest change. Count file types by extension.
3. List problems, each with a count and up to ten examples:
   - files over 2 GB (Rintaro cannot take them yet) and over 10 GB (left alone);
   - names that break the rules: send relative paths to `check_names` with `paths` true, up to 5,000 per call,
     and keep its `fixed` name and problems for each;
   - paths over 240 characters (the same call warns about them);
   - online-only placeholders (cloud files not on this disk), which must be downloaded first or left out;
   - temp and lock files (`~$*`, `*.tmp`, `.~lock*`, `Thumbs.db`, `desktop.ini`, `.DS_Store`), zero-byte files and
     empty folders;
   - likely duplicates (equal size; confirm with a hash only within equal sizes).
4. Write `folder-report.csv` inside `_Rintaro review/<date>/` (path, size, modified, problem, suggested fix) and
   show a short summary: totals, then the problems, biggest first.
5. Offer the next steps (junk, names, duplicates, destinations) one at a time. Change nothing yet.
