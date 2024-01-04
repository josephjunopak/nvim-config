# Custom Neovim Setup

Remaps:
```
vim.g.mapleader = " "
vim.keymap.set("n", "<leader>pv", vim.cmd.Ex)

-- Move highlighted blocks around
vim.keymap.set("v", "J", ":m '>+1<CR>gv=gv")
vim.keymap.set("v", "K", ":m '<-2<CR>gv=gv")

-- Center cursor when going down or up file
vim.keymap.set("n", "<C-d>", "<C-d>zz")
vim.keymap.set("n", "<C-u>", "<C-u>zz")

-- Replace current word in file
vim.keymap.set("n", "<leader>s", [[:%s/\<<C-r><C-w>\>/<C-r><C-w>/gI<Left><Left><Left>]])
```

Telescope:
```
vim.keymap.set('n', '<leader>s/', telescope_live_grep_open_files, { desc = '[S]earch [/] in Open Files' })
vim.keymap.set('n', '<leader>ss', require('telescope.builtin').builtin, { desc = '[S]earch [S]elect Telescope' })
vim.keymap.set('n', '<leader>gf', require('telescope.builtin').git_files, { desc = 'Search [G]it [F]iles' })
vim.keymap.set('n', '<leader>sf', require('telescope.builtin').find_files, { desc = '[S]earch [F]iles' })
vim.keymap.set('n', '<leader>sh', require('telescope.builtin').help_tags, { desc = '[S]earch [H]elp' })
vim.keymap.set('n', '<leader>sw', require('telescope.builtin').grep_string, { desc = '[S]earch current [W]ord' })
vim.keymap.set('n', '<leader>sg', require('telescope.builtin').live_grep, { desc = '[S]earch by [G]rep' })
vim.keymap.set('n', '<leader>sG', ':LiveGrepGitRoot<cr>', { desc = '[S]earch by [G]rep on Git Root' })
vim.keymap.set('n', '<leader>sd', require('telescope.builtin').diagnostics, { desc = '[S]earch [D]iagnostics' })
vim.keymap.set('n', '<leader>sr', require('telescope.builtin').resume, { desc = '[S]earch [R]esume' })
```

Harpoon:
```
 { "<leader>a", function() require("harpoon"):list():append() end, desc = "harpoon file", },
{ "<C-e>", function() local harpoon = require("harpoon") harpoon.ui:toggle_quick_menu(harpoon:list()) end, desc = "harpoon quick menu", },
{ "<leader>1", function() require("harpoon"):list():select(1) end, desc = "harpoon to file 1", },
{ "<leader>2", function() require("harpoon"):list():select(2) end, desc = "harpoon to file 2", },
{ "<leader>3", function() require("harpoon"):list():select(3) end, desc = "harpoon to file 3", },
{ "<leader>4", function() require("harpoon"):list():select(4) end, desc = "harpoon to file 4", },
{ "<leader>5", function() require("harpoon"):list():select(5) end, desc = "harpoon to file 5", },
```
