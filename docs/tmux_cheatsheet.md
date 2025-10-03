# tmux Cheat Sheet

This cheat sheet provides a quick reference for basic tmux commands.

## Prefix Key

All commands in tmux are preceded by a prefix key, which is `Ctrl+b` by default. To send a literal `Ctrl+b`, press `Ctrl+b` twice.

## Sessions

| Command | Description |
| :--- | :--- |
| `tmux new -s {name}` | Create a new named session (from outside tmux). |
| `tmux attach -t {name}` | Attach to a named session (from outside tmux). |
| `tmux ls` | List all running sessions (from outside tmux). |
| `Prefix + d` | Detach from the current session. |
| `Prefix + $` | Rename the current session. |
| `Prefix + s` | List sessions and switch between them. |

## Windows

| Command | Description |
| :--- | :--- |
| `Prefix + c` | Create a new window. |
| `Prefix + p` | Go to the previous window. |
| `Prefix + n` | Go to the next window. |
| `Prefix + {n}` | Go to window number `n` (e.g., Prefix + 1). |
| `Prefix + w` | List all windows in an interactive menu. |
| `Prefix + ,` | Rename the current window. |
| `Prefix + &` | Close the current window (with confirmation). |

## Panes

| Command | Description |
| :--- | :--- |
| `Prefix + %` | Split the current pane vertically (creates a pane on the right). |
| `Prefix + "` | Split the current pane horizontally (creates a pane below). |
| `Prefix + {arrow key}` | Navigate between panes (e.g., Prefix + Up Arrow). |
| `Prefix + o` | Cycle to the next pane in the current window. |
| `Prefix + q` | Briefly show pane numbers for selection. |
| `Prefix + x` | Close the current pane (with confirmation). |
| `Prefix + z` | Toggle zoom for the current pane. |
| `Prefix + Space` | Cycle through the available pane layouts. |
| `Prefix + Alt+{arrow key}` | Resize the current pane (hold Alt and press arrow). |

## Copy Mode (Scrolling and Copying)

| Command | Description |
| :--- | :--- |
| `Prefix + [` | Enter Copy Mode to scroll up and view history. |
| `q` | Quit Copy Mode. |
| `PageUp` / `PageDown` | Scroll up/down by page in Copy Mode. |
| `Space` | Start selection (vi-style keys). |
| `Enter` | Copy the selected text (vi-style keys). |
| `Prefix + ]` | Paste the most recently copied text. |
