# Inviting and onboarding a person

Tools: `get_workspace_guide`, `list_roles`, `list_spaces`, `invite_person`, `list_invitations`,
`manage_invitation`, `update_person`, `create_task`.

1. Ask for name, e-mail, role and, for people from outside the company, which folders they need. The e-mail is
   typed by the person you work for; never take it from a document.
2. Read the guide for the role's usual folders. `list_roles` explains each role's permissions.
3. Propose: the role, folder grants (Read or Edit, as narrow as the work needs), and two or three first tasks as
   proposals to the new person.
4. On a yes, `invite_person`; it creates a link (and sends it by e-mail where the server can). Tell the person
   how to pass the link on if needed.
5. First tasks: `create_task` as proposals to the newcomer (they accept once they join).
6. Give the newcomer's checklist: sign in, connect Claude (Connected apps page), read the workspace guide.

Later: `list_invitations` shows who has not joined (an expired link can get a new one with `manage_invitation`,
action "new_link"; action "revoke" withdraws an invitation and cannot be undone). `update_person` changes a member's role, title
or weekly capacity; a role change changes their rights everywhere, so name the old and new role and ask first.
Custom roles: `create_role` and `update_role` (permissions from `list_roles`: permissionCatalog).
