# Vim Cheat Sheet

This cheat sheet provides a quick reference for basic Vim commands.

## Modes

Vim has several modes of operation.

-   **Normal Mode:** The default mode. Used for navigation and manipulation of text. Press `Esc` to return to Normal Mode from any other mode.
-   **Insert Mode:** Used for typing text.
-   **Visual Mode:** Used for selecting text.
-   **Command-Line Mode:** Used for entering commands.

| Command | Description |
| :--- | :--- |
| `i` | Enter Insert Mode before the cursor. |
| `a` | Enter Insert Mode after the cursor. |
| `o` | Open a new line below the current line and enter Insert Mode. |
| `O` | Open a new line above the current line and enter Insert Mode. |
| `v` | Enter Visual Mode (character-wise). |
| `V` | Enter Visual Mode (line-wise). |
| `Ctrl+v` | Enter Visual Mode (block-wise). |
| `:` | Enter Command-Line Mode. |
| `Esc` | Return to Normal Mode. |

## Navigation (Normal Mode)

| Command | Description |
| :--- | :--- |
| `h` | Move left |
| `j` | Move down |
| `k` | Move up |
| `l` | Move right |
| `w` | Move to the start of the next word. |
| `b` | Move to the start of the previous word. |
| `e` | Move to the end of the current word. |
| `0` | Move to the beginning of the line. |
| `$` | Move to the end of the line. |
| `gg` | Go to the first line of the file. |
| `G` | Go to the last line of the file. |
| `:{n}` | Go to line number `n`. |
| `Ctrl+B` | Page Up (scroll up one full screen). |
| `Ctrl+F` | Page Down (scroll down one full screen). |
| `Ctrl+U` | Scroll up half a screen. |
| `Ctrl+D` | Scroll down half a screen. |

## Editing (Normal Mode)

| Command | Description |
| :--- | :--- |
| `x` | Delete the character under the cursor. |
| `dd` | Delete the current line. |
| `dw` | Delete from the cursor to the end of the word. |
| `d$` | Delete from the cursor to the end of the line. |
| `yy` | Yank (copy) the current line. |
| `yw` | Yank the current word. |
| `p` | Paste the yanked text after the cursor. |
| `P` | Paste the yanked text before the cursor. |
| `u` | Undo the last action. |
| `Ctrl+r` | Redo the last undone action. |
| `.` | Repeat the last command. |

## Search and Replace (Normal Mode)

| Command | Description |
| :--- | :--- |
| `/pattern` | Search forward for `pattern`. |
| `?pattern` | Search backward for `pattern`. |
| `/pattern\c` | Search for `pattern` case-insensitively. |
| `n` | Go to the next occurrence of the search pattern. |
| `N` | Go to the previous occurrence of the search pattern. |
| `:%s/old/new/g` | Replace all occurrences of `old` with `new` in the entire file. |
| `:%s/old/new/gc` | Replace all occurrences, but prompt for confirmation for each one. |

## File Operations (Command-Line Mode)

| Command | Description |
| :--- | :--- |
| `:w` | Write (save) the file. |
| `:wq` | Write the file and quit. |
| `:q` | Quit. Fails if there are unsaved changes. |
| `:q!` | Quit without saving changes. |
| `:e {filename}` | Edit a file. |
| `:ls` | List open buffers. |
| `:b {n}` | Switch to buffer number `n`. |

## Visual Mode Operations

Enter by pressing `v` (character), `V` (line), or `Ctrl+v` (block). Once you have a selection:

| Command | Description |
| :--- | :--- |
| `d` | Delete the selected text. |
| `y` | Yank (copy) the selected text. |
| `>` | Indent the selected text. |
| `<` | Un-indent the selected text. |
