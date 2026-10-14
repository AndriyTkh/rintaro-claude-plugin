# Finding a file

Tools: `search_files`, `list_files`, `get_file`, `list_spaces`, `list_archive`.

1. Turn the request into a few name fragments (a word from the title, a project code, a year the person said).
   `search_files` matches part of the file name in every folder the person can read; contents are not searched.
2. Try two or three fragments. If the person named a folder, use `list_spaces` to find it and `list_files` on it.
3. Show at most five matches, best first: name, folder path, last change and who made it (`get_file` gives the
   path, versions and who uploaded each).
4. Nothing found: say "not found, or not shared with you". Offer to look in the archive (`list_archive`) and to
   ask the folder's responsible person; never suggest that a hidden folder exists.
5. The person wants to open it: offer `get_file_link`, a download link that works for a few minutes and is for
   them only. Do not paste it into shared places.
