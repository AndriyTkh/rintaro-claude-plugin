# Finding a file

Tools: `find_files`, `search`, `list_files`, `get_file`, `list_spaces`, `list_archive` (`search_files` still works,
as a plain name match).

1. Turn the request into a few name fragments (a word from the title, a project code, a year the person said).
   `search` limited to files (kinds: file) ranks files by name across every folder the person can read. It takes
   the web search syntax: several words, prefix*, ~typo, type:pdf, updated:last-30d, owner:me. Contents are not
   searched yet.
2. When the person knows where it is or what it is called, use `find_files` with a glob, as with Glob: a folder
   path, `**` for any depth, `*` within a name, {a,b} for alternatives (for example **/*.{step,stl}). Its path,
   type, added-by and modified-after arguments narrow it. If the person named a folder, `list_spaces` finds it and
   `list_files` lists it.
3. Show at most five matches, best first: name, folder path, last change and who made it (`get_file` gives the
   path, versions and who uploaded each).
4. Nothing found: say "not found, or not shared with you". Offer to look in the archive (`list_archive`) and to
   ask the folder's responsible person; never suggest that a hidden folder exists.
5. The person wants to open it: offer `get_file_link`, a download link that works for a few minutes and is for
   them only. Do not paste it into shared places.
