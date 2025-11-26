# 🌟 Essential Vim Shortcuts (Daily Reference)

Vim operates in several key **Modes**. Most commands below are executed from **Normal Mode**.

1.  **Normal Mode (Default):** For moving, copying, deleting.
2.  **Insert Mode:** For typing text.
3.  **Visual Mode:** For selecting blocks of text.
4.  **Command-Line Mode:** For saving, quitting, and searching (starts with `:`).

---

## 🏃 Movement Commands (Normal Mode)

Navigate quickly without arrow keys.

| Command | Action |
| :--- | :--- |
| `h` | Move **left** |
| `j` | Move **down** |
| `k` | Move **up** |
| `l` | Move **right** |
| `w` | Start of the **next word** |
| `b` | Start of the **previous word** |
| `e` | End of the **current word** |
| `0` (zero) | Start of the **line** |
| `$` | End of the **line** |
| `gg` | To the **very first line** (top of file) |
| `G` | To the **very last line** (bottom of file) |
| `5j` | Move **5 lines down** (prefix a number for repetition) |

---

## 📝 Editing & Insert Commands

### Entering Insert Mode (From Normal Mode)

Press `Esc` to return to Normal Mode after typing.

| Command | Action |
| :--- | :--- |
| `i` | Insert text **before** the cursor |
| `a` | Insert text **after** the cursor |
| `o` | Open a **new line below** |
| `O` | Open a **new line above** |
| `I` | Insert text at the **start of the line** |
| `A` | Insert text at the **end of the line** |

### Deleting and Changing (Normal Mode)

These commands can be combined with Movement commands (e.g., `d` + `w` = `dw`).

| Command | Action |
| :--- | :--- |
| `x` | **Delete** the character under the cursor |
| `dw` | **Delete** from cursor to **end of word** |
| `dd` | **Delete** the **entire current line** |
| `D` | **Delete** from cursor to **end of line** |
| `cw` | **Change** from cursor to **end of word** (deletes, enters Insert Mode) |
| `cc` | **Change** the **entire line** (deletes line, enters Insert Mode) |
| `r` | **Replace** the character under cursor (stays in Normal Mode) |
| `R` | Enter **Replace Mode** (overwrites characters) |

### Copy, Paste, and Undo (Normal Mode)

| Command | Action |
| :--- | :--- |
| `yy` | **Yank** (copy) the **entire current line** |
| `yw` | **Yank** (copy) the **word** under the cursor |
| `p` | **Paste** copied/deleted text **after** cursor/line |
| `P` | **Paste** copied/deleted text **before** cursor/line |
| `u` | **Undo** the last change |
| `Ctrl + r` | **Redo** the last undone change |

---

## 💾 Saving and Quitting (Command-Line Mode)

Press `:` then type the command and `Enter`.

| Command | Action |
| :--- | :--- |
| `:w` | **Write** (save) the file |
| `:q` | **Quit** (exit Vim) |
| `:wq` | **Write** and **Quit** (save and exit) |
| `:x` | Same as `:wq` (save and exit) |
| `:q!` | **Quit** without saving (discard changes) |
| `:wqa` | **Write** and **Quit** all open buffers/files |

---

## 🔎 Searching (Command-Line Mode / Normal Mode)

| Command | Action |
| :--- | :--- |
| `/searchterm` | **Search** forward for the term |
| `?searchterm` | **Search** backward for the term |
| `n` | Go to the **next** match |
| `N` | Go to the **previous** match |
| `:s/old/new/g` | **Substitute** all occurrences of 'old' with 'new' on the **current line** |
| `:%s/old/new/g` | **Substitute** all occurrences of 'old' with 'new' **throughout the entire file** |
