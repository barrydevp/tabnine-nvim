__Note:__ This plugin is in alpha and considered to be unstable. Please do let us know if you're expereicing any issues.

# tabnine-nvim

Tabnine client for neovim

![Tabnine neovim client](https://github.com/codota/tabnine-nvim/blob/master/expamples/javascript.gif)

## Install

Using [vimplug](https://github.com/junegunn/vim-plug)

```
Plug 'codota/tabnine-nvim', { 'do': './dl_binaries.sh' }
```

Basic configuration activation:
```lua
require('tabnine').setup{
  disable_auto_comment=true,
  accept_keymap="<Tab>"
}
```

## Activate Tabnine Pro

`:TabnineHub` - to open Tabnine Hub and log in to your account

## lualine integration

This plugin exposes a lualine `tabnine` component. e.g:

```lua
require'lualine'.setup {
    tabline = {
        lualine_a = {},
        lualine_b = {'branch'},
        lualine_c = {'filename'},
        lualine_x = {},
        lualine_y = {},
        lualine_z = {}
    },
    sections = {lualine_c = {'lsp_progress'}, lualine_x = {'tabnine'}}
}
```

## Known issues

Windows isn't supported yet. PR are welcome!