# nvim-config

Personal Neovim configuration. Leader is `,`.

## Plugins

| Plugin | Purpose |
|--------|---------|
| lazy.nvim | Plugin manager |
| telescope | Fuzzy finder (`f` git files, `F` live grep) |
| treesitter | Syntax highlighting and indentation |
| mini.nvim | File explorer, statusline, text objects (ai) |
| fugitive | `:Git blame` |
| gitsigns | Git diff indicators in sign column |
| git-messenger | `<leader>m` line blame popup |
| which-key | Keybinding hints |
| conform | Format on save, `<leader>f` |
| nvim-lint | Rubocop linting on save |
| copilot | AI inline completions |
| claude-code.nvim | Claude Code terminal in nvim splits |
| vim-endwise | Auto `end` in Ruby |
| vim-sleuth | Auto indent detection |
| indent-blankline | Indent guides |
| dracula | Colorscheme |

## Keybindings

### Navigation

| Key | Action |
|-----|--------|
| `f` | Find git files (telescope) |
| `F` | Live grep (telescope) |
| `<leader>d` | File explorer (mini.files) |
| `<leader><leader>` | Find buffers |
| `<leader>/` | Fuzzy search current buffer |
| `<leader>s_` | Search: help/keymaps/files/grep/diagnostics/resume |

### Git

| Key | Action |
|-----|--------|
| `<leader>b` | Git blame |
| `<leader>m` | Git messenger (line blame popup) |
| `<leader>gs` | Git status (`:G`) |
| `<leader>gj` | Diffget right (`//3`) |
| `<leader>gf` | Diffget left (`//2`) |

### Editing

| Key | Action |
|-----|--------|
| `Y` | Yank to end of line |
| `<leader>y` | Yank to system clipboard |
| `<leader>Y` | Yank to end of line to system clipboard |
| `<leader>,` | Toggle comment |
| `<leader>f` | Format buffer |

### Toggles

| Key | Action |
|-----|--------|
| `<leader>n` | Toggle line numbers + sign column |
| `<leader>w` | Toggle word wrap |
| `<leader>l` | Toggle listchars |

### Windows

| Key | Action |
|-----|--------|
| `C-h/j/k/l` | Move focus between windows |
| `+` / `-` | Resize window height |
| `<leader>+` / `<leader>-` | Resize window width |

### Config

| Key | Action |
|-----|--------|
| `<leader>v` | Edit init.lua |
| `<leader>V` | Browse lua directory |

## Structure

```
init.lua                    Entry point, lazy.nvim bootstrap
lua/config/autocmds.lua     Autocommands
lua/config/keymaps.lua      Key mappings
lua/config/options.lua      Vim options
lua/plugins/*.lua           Plugin specs (one per file)
```
