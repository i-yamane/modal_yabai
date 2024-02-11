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

This `.skhdrc` assumes the Japanese keyboard of Macbooks. In particular, it heavily uses &lt;KANA&gt; and &lt;EISU&gt; keys.
Change the keycodes used in the file appropriately according to your keyboard.

## Usage

### How to start
1. Start `skhd` as a service or directly in a terminal.
I personally execute `skhd -V` from a terminal.
1. Type "&lt;Ctrl&gt;-&lt;KANA&gt; S S" to start a `yabai` service.

### yabai modes
_yabai modes_ are modes defined in `.skhdrc` for interacting with yabai.
- To enter the initial mode _yabai-home-mode_, type "&lt;Ctrl&gt;-&lt;KANA&gt;".

- Follow the instructions in the pop-up window.

- To stop interacting with yabai, type "&lt;Ctrl&gt;-&lt;KANA&gt;".

- To stop the `yabai` service, type "&lt;Ctrl&gt;-&lt;KANA&gt; S Q".

## Tips
### Two-tile view
My favorite command is arranging windows into two vertically split stacks with "&lt;Ctrl&gt;-&lt;KANA&gt; l v".

### Changing focus
You can

- switch the focus between windows with &lt;Cmd&gt;-&lt;Tab&gt; or yabai-focus-mode (&lt;Ctrl&gt;-&lt;KANA&gt; &lt;Tab&gt;)

- and move a window to the other stack "&lt;Ctrl&gt;-&lt;KANA&gt; &lt;Space&gt; &lt;Shift&gt;-h" or "&lt;Ctrl&gt;-&lt;KANA&gt; &lt;Space&gt; &lt;Shift&gt;-l".

### Temporarily maximizing a window
You can temporarily maximize a window with "&lt;Ctrl&gt;-&lt;KANA&gt; l z". The same command brings me back to the two-tile view (it is a toggle command).

## Bugs
Changing focus with "&lt;Ctrl&gt;-&lt;KANA&gt; &lt;Tab&gt; &lt;Shift&gt;-{h, k}" stopped working, but I keep the command there hoping that someone can tell me how to fix it.
