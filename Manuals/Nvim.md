## Keyboard shortcuts
### Cursor motion
- ``H``: Upper left corner (home)
- ``L``: Lower left corner
- ``M``: Middle line
- ``^``: Beginning of line
- ``$``: End of line
- ``1``: Forward one character
- ``w``: One word forward
- ``b``: Back one word
- ``fc``: Find *c*
- ``;``: Repeat find (find next *c*)

### Input
- ``a``: Append after cursor
- ``i``: Insert before cursor
- ``o``: Open line below
- ``O``: Open line above

## Commands
### File management
- ``:w f``: Save file as *f*
- ``:wq``: Exit and save
- ``:x``: Exit and save (if changes have been made)
- ``:w``: Save
- ``:q!`` Exit without saving
- `:xall` Exit all windows and save
### System
- ``:*y``: Copy to the clipboard

## Tools

### File explorer (netrw)
#### How to call
- `:Explore` to open into the entire window
- `:Vexplore` to open with a vertical split

#### Navigation
- `Enter`: Opens a directory or a file.
- `-`: Go up to the parent directory.
- `u`: Go back to the previous directory in the history.
- `gb`: Jump to the most recent directory saved on the "Bookmarks". To create a bookmark we use `mb`.
-  `<C-w>h`: Move to the left window
- `<C-w>l`: Move to the right window
- `<C-w>w`: Cycle through all windows
#### File operations
- `p`: Opens a preview window.
- `<C-w>z`: `Ctrl + w` and then `z`. Closes the preview window.
- `gh`: Toggles the hidden files.
- `%`: Creates a file. Well... it actually doesn't, it just gives you the opportunity to create one. When you press `%` vim will ask the name you want to give the file and then it lets you edit it. After entering the name you have to save the file (using `:write`) to create it.
- `R`: Renames a file
- `mt`: Assign the "target directory" used by the move and copy commands.
- `mf`: Marks a file or directory. Any action that can be performed on multiple files depend on these marks.
- `mc`: Copy the marked files in the target directory.
- `mm`: Move the marked files to the target directory.
- `mx`: Runs an external command on the marked files.
- `D`: Deletes a file or an empty directory. vim will not let us delete a non-empty directory. I'll show how to bypass this later on.
- `d`: Creates a directory.