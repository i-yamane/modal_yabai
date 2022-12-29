# modal_yabai
Modal keybindings for yabai + skhd

## Dependencies
- [yabai](https://github.com/koekeishiya/yabai) (5.0.2)
- [skhd](https://github.com/koekeishiya/skhd) (0.3.5)
- [Hammerspoon](https://github.com/Hammerspoon/hammerspoon) (0.9.97)
- zsh (5.9)

## Installation
Place the content of
- `dot_skhdrc` to `~/.skhdrc`
- `dot_yabairc` to `~/.yabairc`
- `dot_zshenv` to `~/.zshenv`
- `dot_hammerspoon/init.lua` to `~/.hammerspoon/init.lua`

`.skhdrc` assumes the Japanese keyboard of Macbooks.
Change the keycodes used in the file appropriately according to your keyboard.

## Usage

### How to start
1. Start `skhd` as a service or directly on terminal.
I personally use `skhd -V` on terminal.
1. Type "[Ctrl]-[KANA] S S" to start a yabai service.
1. Type "[Ctrl]-[EISU]" to suppress the pop-up window.

### yabai modes
_yabai modes_ are modes defined in `.skhdrc` for interacting with yabai.
- To enter the initial mode _yabai-home-mode_, type "[Ctrl]-[KANA]".
- Follow the instructions in the pop-up window.
- To exit any yabai mode and stop interacting with yabai, type "[Ctrl]-[EISU]".

## Tips
My favorite workflow is
- arranging windows into two stacks with "[Ctrl]-[KANA] l v",
- selecting a window with [CMD]-[TAB] or yabai-focus-mode,
- and moving it to the other stack "[Ctrl]-[KANA] [SPACE] h" or "[Ctrl]-[KANA] [SPACE] l".

When necessary, I temporarily maximize a window with "[Ctrl]-[KANA] l z". The same command brings me back to the two-tile view (it is a toggle command).
