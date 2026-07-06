# FelixKeeb

[中文](README_zh.md)

FelixKeeb is an open-source 5x12+4 split ortholinear keyboard, with 5x6+2 keys on each side.

It is available in both MX and Choc versions. The bottom row can be separated, allowing the keyboard to be built as a smaller mini version.

![FelixKeeb default keymap](keymap-drawer/felix.svg)

## Features

- Split ortholinear layout: 5x12+4, with 5x6+2 keys on each side.
- Switch versions: MX and Choc.
- Mini form factor: the bottom row can be separated for a smaller build.
- Controller: nice!nano / nice!nano v2.
- Battery: 401230 LiPo battery is recommended.
- Display: supports nice!view or OLED.
- Firmware: powered by ZMK with wireless Bluetooth support.
- Key remapping: supports ZMK Studio and [Nick Coutsos Keymap Editor](https://nickcoutsos.github.io/keymap-editor/).

## Branches

| Branch | Description |
| --- | --- |
| `master` | Standard 5x12+4 version |
| `36` | 4x12+2 version |
| `prospector-dongle` | 5x12+4 dongle version using [prospector](https://github.com/carrefinho/prospector) as the receiver |

## Default Keymap

The default keymap is shown in [keymap-drawer/felix.svg](keymap-drawer/felix.svg).

The keymap source is located at [config/felix.keymap](config/felix.keymap), and the keyboard layout JSON is located at [config/felix.json](config/felix.json).

## Key Remapping

You can remap the keyboard with the following tools:

- [ZMK Studio](https://zmk.dev/docs/features/studio)
- [Nick Coutsos Keymap Editor](https://nickcoutsos.github.io/keymap-editor/)

The build configuration in this repository already includes the `studio-rpc-usb-uart` snippet required by ZMK Studio.

## Firmware Build

GitHub Actions generates the build matrix from [build.yaml](build.yaml). By default, it builds the following firmware files:

- `felix_left nice_oled`
- `felix_right nice_oled`
- `settings_reset`
- `felix_left nice_view_adapter nice_epaper`
- `felix_right nice_view_adapter nice_epaper`

Before flashing, choose the build artifact that matches your hardware version.

## Hardware

| Item | Configuration |
| --- | --- |
| Keyboard type | Split ortholinear |
| Layout | 5x12+4, 5x6+2 on each side |
| Controller | nice!nano / nice!nano v2 |
| Battery | 401230 |
| Display | nice!view / OLED |
| Firmware | ZMK |
| Key remapping tools | ZMK Studio / Nick Coutsos Keymap Editor |

## Credits

FelixKeeb is built on the ZMK ecosystem. Thanks to the ZMK project, nice!nano, nice!view, and all open-source hardware and firmware contributors in the community.
