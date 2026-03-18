# Keychron on Linux

Community-maintained guides for using Keychron keyboards on Linux.

## Keyboards

- **[Keychron K2](k2.md)** -- 75% layout, compact with function row
- **[Keychron K6](k6.md)** -- 65% layout, no function row

## Quick Start

Most issues boil down to three things:

1. **Set the physical switch to Windows/Android mode** (back of keyboard)
2. **Function keys should work out of the box on kernel 5.19+** thanks to `fnmode=3` auto-detection
3. **Bluetooth reconnection problems?** See the Bluetooth section in your keyboard's page

## Original vs Pro (QMK) Models

Keychron ships two variants of many keyboards. They have very different Linux experiences:

| | Original | Pro (QMK) |
|---|---|---|
| Kernel driver | `hid-apple` | `hid-generic` |
| Function keys | `fnmode` parameter | Configured via VIA/Launcher |
| Firmware updates | Windows only | Linux via Keychron Launcher |
| Key remapping | `keyd`, `xremap`, XKB | VIA, Keychron Launcher |
| RGB control | Hardware shortcuts only | VIA/Launcher (wired) |

If you have a Pro model, the `hid_apple` kernel module parameters (`fnmode`, `swap_opt_cmd`, etc.) **do not apply** to you. Use [Keychron Launcher](https://launcher.keychron.com/) or [VIA](https://usevia.app/) instead (Chromium required, wired connection only).

## Contributing

Pull requests welcome. If you have a tip, fix, or workaround, open a PR or file an issue.

## Resources

- [andrebrait's Keychron Linux guide](https://gist.github.com/andrebrait/961cefe730f4a2c41f57911e6195e444) -- the most comprehensive community resource
- [Arch Wiki: Apple Keyboard](https://wiki.archlinux.org/title/Apple_Keyboard) -- covers `hid_apple` parameters
- [Arch Wiki: Bluetooth keyboard](https://wiki.archlinux.org/title/Bluetooth_keyboard) -- generic BT pairing/troubleshooting
- [keyd](https://github.com/rvaiya/keyd) -- system-wide key remapping daemon (X11, Wayland, TTY)
- [Keychron Launcher](https://launcher.keychron.com/) -- web-based configuration for QMK boards
- [r/Keychron](https://www.reddit.com/r/Keychron/) -- community subreddit

## License

[MIT](LICENSE) -- originally by [kurgol](https://github.com/kurgol/keychron).
