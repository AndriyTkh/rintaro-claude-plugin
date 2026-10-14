# Access audit

Tools: `access_report`, `list_spaces`, `get_space_access`.

1. `access_report` without a folder: flags over every folder the person manages, and how many folders they can
   see but do not manage (those cannot be audited by them; suggest asking the Owner).
2. Flags to explain in plain words:
   - Everyone can open a folder whose name looks private (HR, finance, contracts ...);
   - people from outside the company (a role without company access) can edit;
   - a Restricted folder whose responsible person has left.
3. Add a per-folder overview for the top-level folders: who can open each and why (`access_report` with `spaceId`).
4. Fixes go through the sharing workflow of this skill, one folder at a time, each with its own yes. The audit
   itself changes nothing.
