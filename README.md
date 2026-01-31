# LXQt-scripts

## kbd_backlight

A small script to get or set the keyboard backlight via UPower (for LXQt on X11).

### Installation

- Copy the script to `~/.local/bin`
- Ensure `~/.local/bin` is in your `PATH` (add to `~/.profile` or `~/.bashrc` if needed).

### Usage

- Increase keyboard backlight by 15: `kbd_backlight +15`
- Decrease keyboard backlight by 15: `kbd_backlight -15`
- Set an absolute keyboard backlight value (integer): `kbd_backlight 150`

### Integration with LXQt

- Open LXQt Global Actions (lxqt-config-globalkeyshortcuts).
- Create a keyboard shortcut to increase backlight, command: `kbd_backlight +15`
- Create a keyboard shortcut to decrease backlight, command: `kbd_backlight -15`

### Notes

- The script requires gdbus and access to the system D-Bus org.freedesktop.UPower KbdBacklight object.
- Argument must be an integer, optionally prefixed with + or - for relative changes.
- The value will be clamped to the device-supported range.
