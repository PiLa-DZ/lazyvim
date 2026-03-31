# Disable diagnostics specifically for markdown files

The "Pure Lua" Autocmd (The Simplest Way)

If you want a "set it and forget it" solution
that doesn't depend on complex plugin logic,
you can add a simple Autocommand to your lua/config/autocmds.lua file.

```lua
-- lua/config/autocmds.lua
-- INFO: Disable diagnostics specifically for markdown files
vim.api.nvim_create_autocmd("FileType", {
  pattern = "markdown",
  callback = function()
    vim.diagnostic.enable(false)
  end,
})
```
