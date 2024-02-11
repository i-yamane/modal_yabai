# `modal_yabai`
Modal keybindings
  - for `yabai` (titling window manager for macOS)
  - with `skhd` (hotkey daemon for macOS).

## Dependencies
- [`yabai`](https://github.com/koekeishiya/yabai) (5.0.2)
- [`skhd`](https://github.com/koekeishiya/skhd) (0.3.5)
- [`Hammerspoon`](https://github.com/Hammerspoon/hammerspoon) (0.9.97)
- `zsh` (5.9)

### Note
- It should be easy to migrate from `zsh` to any common shell.
- Hammerspoon is used to show hints on the keybindings in a pop-up window. If you don't need it, you can use `modal_yabai` without it.

## Installation
Place the content of
- `dot_skhdrc` to `~/.skhdrc`
- `dot_yabairc` to `~/.yabairc`
- `dot_zshenv` to `~/.zshenv`
- `dot_hammerspoon/init.lua` to `~/.hammerspoon/init.lua`

This `.skhdrc` assumes the Japanese keyboard of Macbooks. In particular, it heavily uses <KANA> and <EISU> keys.
Change the keycodes used in the file appropriately according to your keyboard.

## Usage

### How to start
1. Start `skhd` as a service or directly in a terminal.
I personally execute `skhd -V` from a terminal.
1. Type "<Ctrl>-<KANA> S S" to start a yabai service.
1. Type "<Ctrl>-<EISU>" to stop interacting with `modal_yabai`.

### yabai modes
_yabai modes_ are modes defined in `.skhdrc` for interacting with yabai.
- To enter the initial mode _yabai-home-mode_, type "[Ctrl]-[KANA]".
- Follow the instructions in the pop-up window.
- To exit any yabai mode and stop interacting with yabai, type "[Ctrl]-[EISU]".

## Tips
### Two-tile view
My favorite command is arranging windows into two vertically split stacks with "<Ctrl>-<KANA> l v".

### Changing focus
You can
- switch the focus between windows with <Cmd>-<Tab> or yabai-focus-mode (<Ctrl>-<KANA> <Tab>)
- or move it to the other stack "<Ctrl>-<KANA> <Space> <Shift>-h" or "<Ctrl>-<KANA> <Space> <Shift>-l".

### Temporarily maximizing a window
You can temporarily maximize a window with "<Ctrl>-<KANA> l z". The same command brings me back to the two-tile view (it is a toggle command).

## Bugs
Changing focus with "<Ctrl>-<KANA> <Tab> <Shift>-{h, k}" stopped working, but I keep the command there hoping that someone can tell me how to fix it.
