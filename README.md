# Custom Neovim Setup

Remap:
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
'<leader>pf' - Find files
'<C-p>' - Only look at files in Git
'<leader>ps' - Grep >
```

Harpoon:
```
'<leader>a' -k Add current file to Harpoon menu
'<C-e' - Toggle Harpoon menu

'<C-h>' - Go to file 1
'<C-t>' - Go to file 2
'<C-n>' - Go to file 3
'<C-s>' - Go to file 4
```

Undotree:
```
'<leader>u' - Opens UndoTree
```

Fugitve:
```
'<leader>gs' - Git Menu
```
