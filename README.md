git-extract-files
=================

Extracts files from current repo to a new repo, keeping ONLY the history for those files.
A new git repo is created at destination-dir, and the entire contents of the current repo are pull'd over. Then, a filter-branch is executed to edit history to only include changes to the selected files. Finally, empty commits are purged. The end result should be a repo with a history containing ONLY edits to the selected files.

Usage:
  
    git-extract-files [destination-dir] [<file> ...]
    
    
Known issues:
- History doesn't seem to track well across file renames - all history before the rename will be obliterated.
    
  
