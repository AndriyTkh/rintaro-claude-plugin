# Rintaro for Claude

This plugin connects Claude to Rintaro, the team's work OS. It holds no data and no secrets: only the address of the
Rintaro server and short skills. Everything Claude learns about your work comes from Rintaro at the
time you ask, with exactly the rights you have in Rintaro, and every change Claude makes shows as made by Claude for
you and can be undone.

## Connect

The Connected apps page in Rintaro shows the one step for the Claude app you use. In short:

- **Claude Code:** install the plugin with the command shown on that page, then type `/mcp`, choose rintaro,
  **Authenticate**, sign in to Rintaro and **Allow**.
- **Claude app (Pro or Max):** Customize, Plugins, add this marketplace or upload the plugin zip; then the plugin's
  Connectors tab, **Add**, **Connect**, sign in to Rintaro and **Allow**.

Routines such as a weekly plan, a deadlines digest or a health check come from the Rintaro server as prompts; in Claude
Code they appear as `/rintaro:` commands.

## Skills

Claude picks a skill by itself when your request fits it; there is nothing to switch on. Each skill is a short
workflow; the work itself is done by Rintaro's tools, with your rights.

| Skill | For |
|---|---|
| managing-rintaro-files | Finding files, filing an import, storage, duplicates, getting an archived file back |
| reorganizing-folders | Moving, renaming and merging folders or reshaping a task tree, as a plan you confirm |
| preparing-files-for-sync | Getting a folder on your computer ready for Rintaro (names, junk, duplicates, large files), then uploading it with the upload tools |
| checking-sync-and-health | A health check of the workspace or your own work; sync status comes with Rintaro Sync |
| planning-work-and-deadlines | Your day or week, deadlines, tasks from notes, a new grant or event, timesheets |
| managing-access-and-people | Sharing a folder, explaining who sees what and why, access audits, a new colleague |
| reporting-on-work | Weekly status, catching up after time away, hours, grant progress |

Bigger changes (many moves, renames or task edits) are shown first as a plan, with who would gain or lose access.
Nothing changes until you say yes, and the whole plan can be undone in one step. Claude never deletes: it archives,
and archived items can be restored.

Maintainers: `evals/` holds the test cases for `claude plugin eval` (trigger, near-miss and behaviour cases per
skill, in English and Ukrainian). It is not part of the installed plugin.

## Privacy

Rintaro data in a Claude conversation is yours to look after: do not share such chats with people outside your
workspace, and keep model training off in your Claude privacy settings.
