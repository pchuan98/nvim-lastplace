# nvim-lastplace

> frok from [ethanholz/nvim-lastplace](https://github.com/ethanholz/nvim-lastplace)

## requirements

- nvim version 7.0 or greater
- lazy.nvim

## fixed and append

- Added ignore_extension for recognition of file extensions.

## usage

```lua
return { 
    "pchuan98/nvim-lastplace",
    lazy = false,
    config = function()
        local opts = {
            lastplace_ignore_buftype = {"quickfix", "nofile", "help"},
            lastplace_ignore_filetype = {"gitcommit", "gitrebase", "svn", "hgcommit"},
            lastplace_open_folds = true,
            ignore_extension = {"py"}
        }
        require("nvim-lastplace").setup(opts)
    end
}
```