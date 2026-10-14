# Very large and very old files

Tools: the local file tools.

1. Very large: list files over 2 GB (Rintaro cannot take them) and over 10 GB (never touched). For each, offer:
   keep it out of the sync, or keep it local and upload a compressed copy (the original stays). The person decides.
2. Old: list files not changed for several years (ask how many; three is a good default). Offer to move them to an
   `Archive/<year>` subfolder inside the same folder, so they sync but stay out of the way.
3. Show counts and sizes, wait for an explicit yes, log every move in `_Rintaro review/<date>/changes.csv`, and
   move in batches of at most 200 items or 20 GB.
