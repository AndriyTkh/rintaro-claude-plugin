{
 "planId": "plan-demo",
 "expiresAt": "in 24 hours",
 "items": [
  {
   "index": 0,
   "op": "{{input.changes.0.op}}",
   "kind": "{{input.changes.0.kind}}",
   "what": "the first change as asked",
   "status": "ok",
   "files": 3,
   "bytes": 2400000,
   "access": [
    {
     "personId": "p-olha",
     "name": "Olha K.",
     "before": "read",
     "after": "none"
    }
   ],
   "accessMore": 0,
   "subfoldersChanged": 0
  }
 ],
 "totals": {
  "changes": 1,
  "accepted": 1,
  "unchanged": 0,
  "refused": 0,
  "files": 3,
  "bytes": 2400000,
  "peopleGaining": 0,
  "peopleLosing": 1
 },
 "limits": {
  "maxItems": 200,
  "maxBytes": 20000000000
 },
 "notes": [
  "Nothing has changed yet. apply_plan carries this plan out once the person chooses it (no second confirmation)."
 ]
}
