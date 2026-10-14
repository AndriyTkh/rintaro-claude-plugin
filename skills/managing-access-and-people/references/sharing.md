# Sharing a folder, or explaining access

Tools: `list_spaces`, `access_report`, `get_space_access`, `list_roles`, `list_people`, `change_space_grant`,
`set_space_grants`, `list_access_requests`, `access_request`, `undo_change`.

1. Find the folder (`list_spaces`). Not there: "not found or not shared with you".
2. `access_report` with `spaceId` (needs manage on the folder): inherits or overrides, Restricted, grants here and
   inherited, the result per role, and every person who can open it. Without manage, say who manages it (the
   folder's responsible person) and stop.
3. "Why can't my colleague see it?": find their role (`list_people`) and walk the reasons: no grant for Everyone,
   their role or them; a Restricted folder above; a narrower grant nearer the folder.
4. Propose the smallest change: a person grant before a role grant; Read before Edit; a grant on this folder
   before one on the parent. Say the effect: who gains or loses, and that subfolders inherit it unless they set
   their own.
5. One subject at a time: `change_space_grant` gives, changes or removes the grant of one person, role or Everyone
   and keeps the others ("none" blocks inherited access; "remove" lets inheritance apply again). Only for several
   subjects or Restricted use `set_space_grants`, which replaces the folder's whole list: send the current grants
   plus the change, never a partial list. Manage, Everyone and Restricted need a second yes because they reach far.
6. Check with `access_report` again and give the activity id for undo.

Access requests: `list_access_requests` shows the open ones the person may answer. Answer with `access_request`
(`grant` or `refuse`) only after they say which; a grant is a person grant on that folder, undoable with its
activity id. To ask for access for the person themselves, `access_request` with `ask`.
