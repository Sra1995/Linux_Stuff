# Arch Linux & Terminal Survival Cheat Sheet

## 1. Package Management (Pacman)
*Everything you need to keep your system updated and clean.*

### Updates & Installation
| Command | Description |
| :--- | :--- |
| `sudo pacman -Syu` | **Update the entire system.** (Run this frequently) |
| `sudo pacman -S [package]` | Install a specific package (e.g., `sudo pacman -S vlc`). |
| `pacman -Ss [keyword]` | Search the repositories for a package. |
| `pacman -Qi [package]` | Show detailed info about an installed package. |

### Cleaning & Maintenance
| Command | Description |
| :--- | :--- |
| `sudo pacman -Rns [package]` | **Remove** a package, its config, and unneeded dependencies. |
| `pacman -Qdt` | **List "Orphans"** (useless dependencies installed by apps you removed). |
| `sudo pacman -Rns $(pacman -Qdtq)`| **Nuke Orphans:** Automatically remove all orphans found above. |
| `paccache -r` | Clean package cache (keeps last 3 versions). Requires `pacman-contrib`. |

---

## 2. File System Navigation
*Moving around your computer folders.*

### The `ls` Command (List)
| Command | Description |
| :--- | :--- |
| `ls` | List files in current directory. |
| `ls -l` | List in "Long" format (shows permissions, owner, file size). |
| `ls -a` | Show **All** files (including hidden dotfiles like `.bashrc`). |
| `ls -lh` | Long format with **Human-readable** sizes (MB, GB, etc). |

### The `cd` Command (Change Directory)
| Command | Description |
| :--- | :--- |
| `cd /path/to/folder` | Go to a specific folder. |
| `cd ..` | Go **Up** one level (e.g., from `/home/sammie` to `/home`). |
| `cd ~` | Go to your **Home** folder (`/home/sammie`). |
| `cd -` | Go back to the **Previous** directory you were just in. |
| `pwd` | **Print Working Directory** (Where am I right now?). |

---

## 3. Text Editors
*How to edit config files without a mouse.*

### Option A: Nano (Beginner Friendly)
*Commands usually displayed at the bottom of the screen. `^` means `Ctrl`.*

**Command:** `nano filename.txt`

| Action | Shortcut |
| :--- | :--- |
| **Save File** | `Ctrl` + `O` (Then hit Enter) |
| **Exit Nano** | `Ctrl` + `X` |
| **Search Text** | `Ctrl` + `W` (Type query, hit Enter) |
| **Cut Line** | `Ctrl` + `K` |
| **Paste Line** | `Ctrl` + `U` |

### Option B: Vim (Power User)
*Vim has "Modes". You start in **Normal Mode** (cannot type text).*

**Command:** `vim filename.txt`

#### 1. Mode Switching
* **`i`** → Switch to **Insert Mode** (Type text like normal).
* **`Esc`** → Switch back to **Normal Mode** (Run commands).

#### 2. Saving & Quitting (Must be in Normal Mode)
| Command | Description |
| :--- | :--- |
| `:w` | **Write** (Save). |
| `:q` | **Quit**. |
| `:wq` | **Write & Quit** (Save and exit). |
| `:q!` | **Force Quit** (Exit *without* saving changes). |

#### 3. Editing & Navigation (In Normal Mode)
| Key | Action |
| :--- | :--- |
| `dd` | **Delete** (Cut) the current line. |
| `yy` | **Yank** (Copy) the current line. |
| `p` | **Paste** the line below cursor. |
| `u` | **Undo** last change. |
| `/word` | **Search** for "word" (Press `n` for next match). |
