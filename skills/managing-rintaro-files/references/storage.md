# Storage use

Tools: `storage_report`, `find_duplicates`, `list_archive`.

1. Call `storage_report` (whole workspace, or `spaceId` for one folder). It counts only folders the person can
   read; say so when the person asks about "all" storage.
2. Show: total size of current files, the share taken by older versions, the archive's share, the five biggest
   folders and the largest files, in GB or MB with one decimal.
3. Ways to save space, as suggestions only:
   - duplicates (`find_duplicates`, then the duplicates workflow of this skill);
   - very large files that belong elsewhere (move them through a plan);
   - the archive: only the Owner can purge it, in the web app. Never offer to purge.
4. Change nothing in this workflow.
