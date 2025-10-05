# nvim-config
Neovim Configuration.

This repository contains a custom Neovim configuration (init.lua) designed for efficient text editing, file navigation, and syntax highlighting. It uses modern Neovim plugins managed by lazy.nvim to provide a lightweight, extensible setup with a clean user interface.
Features

Indentation Settings: Configured for 2-space indentation with expandtab, tabstop=2, softtabstop=2, and shiftwidth=2 for consistent code formatting.
Custom Keybindings:
Insert mode mappings for ASCII art (e.g., <A-k> for `├──`, <A-i> for `│`, <A-l> for `└──`) to aid in creating visual hierarchies.
Normal mode mappings:
<C-p>: Opens Telescope file finder.
<leader>fg: Runs Telescope live grep for searching across files.
<C-n>: Toggles Neo-tree filesystem explorer on the left.


Leader key set to <Space> for easy access to custom mappings.


**Plugin Management**: Uses lazy.nvim for lazy-loading plugins, with automatic installation and updates enabled.
Plugins:
_catppuccin/nvim_: Provides the Catppuccin colorscheme for a modern, visually appealing look.
_nvim-telescope/telescope.nvim_: Fuzzy finder for files and text, with plenary.nvim as a dependency.
_nvim-treesitter/nvim-treesitter_: Syntax highlighting and indentation for languages like Lua, JavaScript, Python, C, Markdown, and more.
_nvim-neo-tree/neo-tree.nvim_: File explorer with dependencies (plenary.nvim, nui.nvim, nvim-web-devicons) for a rich filesystem view.


**Colorscheme**: Defaults to Catppuccin, with habamax as a fallback during plugin installation.
Treesitter: Configured for syntax highlighting and indentation across multiple languages, with automatic installation of parsers.

### Installation

Install Neovim: Ensure you have Neovim (version 0.9 or later) installed. Download it from Neovim's GitHub releases or use a package manager:
# On Ubuntu/Debian
```
sudo apt install neovim
```
# On macOS
```
brew install neovim
```


## Clone this Repository:
git clone https://github.com/your-username/your-repo-name.git ~/.config/nvim


Start Neovim:
nvim

On first launch, lazy.nvim will automatically clone itself and install the specified plugins. If the cloning fails, an error message will prompt you to press a key to exit.

**Verify Plugin Installation:**

Run :Lazy to open the lazy.nvim interface and check plugin status.
Ensure all plugins (catppuccin, telescope.nvim, nvim-treesitter, neo-tree.nvim) are installed and loaded.



### Usage

**File Navigation:**
Press <C-p> to open Telescope and search for files.
Press <leader>fg (default: <Space>fg) to search file contents with live grep.
Press <C-n> to toggle the Neo-tree filesystem explorer.


### ASCII Art Shortcuts:
In insert mode, use <A-k> (Alt+k) for ├──, <A-i> for │, and <A-l> for └── to create tree-like structures.


Leader Key: Set to <Space> for all leader-based mappings. Local leader is set to \.
Syntax Highlighting: Treesitter automatically highlights supported languages (Lua, JavaScript, Python, etc.).
Plugin Updates: lazy.nvim checks for updates automatically. Run :Lazy update to manually trigger updates.

### File Structure

init.lua: The main Neovim configuration file, included below for reference.
Plugins are installed in ~/.local/share/nvim/lazy/ (or equivalent, based on your system).

### Dependencies

Neovim: Version 0.9 or higher.
Git: Required for cloning lazy.nvim and plugins.
Optional: ripgrep for faster Telescope live grep searches.

### Customization
To modify this configuration:

Edit init.lua in ~/.config/nvim/.
Add or remove plugins in the lazy.nvim spec table.
Adjust keybindings or settings as needed.
Run :Lazy sync to apply plugin changes.

### For plugin-specific documentation:

lazy.nvim
catppuccin
telescope.nvim
nvim-treesitter
neo-tree.nvim

### Troubleshooting

Plugins not loading: Run :Lazy check to verify plugin status. Ensure Git is installed and accessible.
Colorscheme issues: Confirm catppuccin is installed via :Lazy. If it fails, the fallback habamax will be used.
Keybinding conflicts: Check for overlapping mappings with :map or redefine them in init.lua.
Treesitter errors: Run :TSUpdate to update language parsers.
