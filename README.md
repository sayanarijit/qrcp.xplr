[![xplr-qr.gif](https://s4.gifyu.com/images/xplr-qr.gif)](https://gifyu.com/image/rGzL)

## Requirements

- [qrcp](https://github.com/claudiodangelis/qrcp)

## Installation

### Install manually

- Add the following line in `~/.config/xplr/init.lua`

  ```lua
  local home = os.getenv("HOME")
  package.path = home
  .. "/.config/xplr/plugins/?/init.lua;"
  .. home
  .. "/.config/xplr/plugins/?.lua;"
  .. package.path
  ```

- Clone the plugin

  ```bash
  mkdir -p ~/.config/xplr/plugins

  git clone https://github.com/sayanarijit/qrcp.xplr ~/.config/xplr/plugins/qrcp
  ```

- Require the module in `~/.config/xplr/init.lua`

  ```lua
  require("qrcp").setup()

  -- Or

  require("qrcp").setup{
    mode = "action",
    key = "Q",
    send_options = "-i wlp2s0",
    receive_options = "-i wlp2s0",
  }

  -- Type `:Q` to send or receive files.
  ```

## Features

- Select multiple files and send.
