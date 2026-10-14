{
 "spaces": [
  {
   "id": "sp-import",
   "parentId": null,
   "name": "Import",
   "path": [],
   "myLevel": "manage",
   "grants": [],
   "restricted": false
  },
  {
   "id": "sp-contracts",
   "parentId": null,
   "name": "Contracts",
   "path": [],
   "myLevel": "manage",
   "grants": [
    {
     "roleKey": "admin",
     "level": "write"
    }
   ],
   "restricted": false
  },
  {
   "id": "sp-projects",
   "parentId": null,
   "name": "Projects",
   "path": [],
   "myLevel": "manage",
   "grants": [
    {
     "everyone": true,
     "level": "read"
    }
   ],
   "restricted": false
  },
  {
   "id": "sp-drafts",
   "parentId": "sp-projects",
   "name": "Drafts",
   "path": [
    "Projects"
   ],
   "myLevel": "manage",
   "grants": [],
   "restricted": false
  },
  {
   "id": "sp-old",
   "parentId": "sp-projects",
   "name": "Old Projects",
   "path": [
    "Projects"
   ],
   "myLevel": "manage",
   "grants": [],
   "restricted": false
  },
  {
   "id": "sp-archive",
   "parentId": null,
   "name": "Archive",
   "path": [],
   "myLevel": "manage",
   "grants": [],
   "restricted": true
  },
  {
   "id": "sp-brand",
   "parentId": null,
   "name": "Brand",
   "path": [],
   "myLevel": "manage",
   "grants": [
    {
     "roleKey": "marketing",
     "level": "read"
    }
   ],
   "restricted": false
  },
  {
   "id": "sp-hr",
   "parentId": null,
   "name": "HR",
   "path": [],
   "myLevel": "manage",
   "grants": [],
   "restricted": true
  }
 ]
}
