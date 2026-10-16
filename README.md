# Tmux Configuration (.config-tmux)

A modern, high-performance, and visually polished Tmux configuration styled with the **Catppuccin Macchiato** color palette to seamlessly match Neovim and terminal workflows.

---

## 📂 Project Structure

```text
~/.config/tmux/
├── .gitignore          # Ignores local plugin installs (plugins/)
├── README.md           # Documentation
└── tmux.conf           # Main tmux configuration file
```

---

## 🎨 Theme & Appearance
- **Palette:** Catppuccin Macchiato (`#24273a` background, `#8aadf4` blue accents, `#363a4f` surface highlights).
- **Status Bar:** Positioned at the **top**, featuring session badge (`󰙯`), date (`󰃰`), and live clock (`󱑂`).
- **Window Tabs:** Rounded powerline style with active/inactive indicators and 1-based indexing.
- **Panes:** Highlighted active pane border (`#8aadf4`) and subtle inactive borders (`#363a4f`).

---

## ⚙️ General Settings & Performance
- **True Color Support:** Full 24-bit RGB true color rendering (`screen-256color` with RGB overrides).
- **Escape Delay:** Set to `0ms` (`set -sg escape-time 0`) for instant `Esc` response in Neovim.
- **Mouse Support:** Fully enabled (`set -g mouse on`) for scrolling, pane resizing, and selection.
- **Window/Pane Indexing:** Starts at `1` (instead of `0`) with automatic renumbering when closed.
- **History Limit:** Expanded to 50,000 lines.

---

## ⌨️ Keybindings & Shortcuts

Prefix Key: `Ctrl+a` (overrides default `Ctrl+b`)

### General & Management
| Shortcut | Action |
| :--- | :--- |
| `Ctrl+a` then `r` | Reload tmux configuration (`~/.config/tmux/tmux.conf`) |
| `Ctrl+a` then `I` | Install/update TPM plugins |

### Panes & Splitting
| Shortcut | Action |
| :--- | :--- |
| `Ctrl+a` then `\|` | Split pane horizontally (current path) |
| `Ctrl+a` then `-` | Split pane vertically (current path) |

### Vim-Style Pane Navigation
| Shortcut | Action |
| :--- | :--- |
| `Ctrl+a` then `h` | Move to left pane |
| `Ctrl+a` then `j` | Move to bottom pane |
| `Ctrl+a` then `k` | Move to top pane |
| `Ctrl+a` then `l` | Move to right pane |

### Copy Mode (Vi Mode)
| Shortcut | Action |
| :--- | :--- |
| `Ctrl+a` then `[` | Enter copy mode |
| `v` (in copy mode) | Begin visual selection |
| `y` (in copy mode) | Yank selection to clipboard (`tmux-yank`) |

---

## 🔌 Plugins (via TPM)
Managed via [Tmux Plugin Manager (TPM)](https://github.com/tmux-plugins/tpm):
- `tmux-plugins/tpm` — Plugin manager
- `tmux-plugins/tmux-sensible` — Basic sensible defaults
- `tmux-plugins/tmux-yank` — OS clipboard integration
