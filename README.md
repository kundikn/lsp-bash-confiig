# lsp-bash-confiig

Как это выглядит
![image](https://github.com/user-attachments/assets/a44f0033-1cdf-4281-b318-5a6530f808eb)

### Установка
*Распаковать архив lsp-config.tar.gz и поместить папку nvim в .config*

*Установить nvim > 0.10.* - обязательно

*Установить утилиты*
```bash
sudo apt update
sudo apt install -y curl git unzip gcc build-essential nodejs npm \
  ripgrep fd-find python3 python3-pip shfmt

npm install -g bash-language-server
```

*Открыть nvim, выполнить :Lazy sync*

*Далее можно развлекаться*

### Установленные плагины:
- `nvim-lspconfig` — для LSP
- `nvim-cmp` — автодополнение
- `LuaSnip` + `friendly-snippets` — сниппеты (например, `if` + `<Tab>` превращается в конструкцию `if ... fi` в bash)
- `telescope.nvim` — быстрый fuzzy-поиск файлов
- `nvim-tree` — файловый менеджер сбоку
- `formatter.nvim` — автоформатирование (например, bash через `shfmt`)
- `gruvbox` — любимая тёмная тема
- `treesitter` — улучшенная подсветка кода

Для того чтобы настроить переход фокуса с файла на дерево необходимо в `.config/nvim/lua/plugins.lua` добавть комбинацию в `"nvim-tree/nvim-tree.lua"`:
```
vim.keymap.set("n", "<leader>e", ":NvimTreeFocus<CR>", { silent = true })
```
