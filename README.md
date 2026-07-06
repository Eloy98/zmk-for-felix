# FelixKeeb

FelixKeeb is an open-source 5x12+4 split ortholinear keyboard, with 5x6+2 keys on each side.

FelixKeeb 是一把开源的 5x12+4 分体正交键盘，左右两侧各为 5x6+2。

It is available in both MX and Choc versions. The bottom row can be separated, allowing the keyboard to be built as a smaller mini version.

键盘提供 MX 与 Choc 两个版本。最下面一行支持拆分，可组装为更小巧的 mini 版本。

![FelixKeeb 默认布局](keymap-drawer/felix.svg)

## Features / 特性

- Split ortholinear layout: 5x12+4, with 5x6+2 keys on each side.  
  分体正交布局：5x12+4，左右各 5x6+2。
- Switch versions: MX and Choc.  
  轴体版本：支持 MX 版本和 Choc 版本。
- Mini form factor: the bottom row can be separated for a smaller build.  
  Mini 形态：最下面一行支持拆分，可按需组装为 mini 版本。
- Controller: nice!nano / nice!nano v2.  
  主控：nice!nano / nice!nano v2。
- Battery: 401230 LiPo battery is recommended.  
  电池：推荐 401230 规格锂电池。
- Display: supports nice!view or OLED.  
  显示屏：支持 nice!view 或 OLED。
- Firmware: powered by ZMK with wireless Bluetooth support.  
  固件：基于 ZMK，支持蓝牙无线使用。
- Key remapping: supports ZMK Studio and [Nick Coutsos Keymap Editor](https://nickcoutsos.github.io/keymap-editor/).  
  改键：支持 ZMK Studio，也支持 [Nick Coutsos Keymap Editor](https://nickcoutsos.github.io/keymap-editor/)。

## Branches / 分支说明

| Branch / 分支 | Description / 说明 |
| --- | --- |
| `master` | Standard 5x12+4 version / 5x12+4 标准版本 |
| `36` | 4x12+2 version / 4x12+2 版本 |
| `prospector-dongle` | 5x12+4 dongle version using [prospector](https://github.com/carrefinho/prospector) as the receiver / 5x12+4 dongle 版本，接收器使用 [prospector](https://github.com/carrefinho/prospector) |

## Default Keymap / 默认布局

The default keymap is shown in [keymap-drawer/felix.svg](keymap-drawer/felix.svg).

默认键位图见 [keymap-drawer/felix.svg](keymap-drawer/felix.svg)。

The keymap source is located at [config/felix.keymap](config/felix.keymap), and the keyboard layout JSON is located at [config/felix.json](config/felix.json).

键位源码位于 [config/felix.keymap](config/felix.keymap)，键盘布局 JSON 位于 [config/felix.json](config/felix.json)。

## Key Remapping / 在线改键

You can remap the keyboard with the following tools:

你可以使用以下工具调整键位：

- [ZMK Studio](https://zmk.dev/docs/features/studio)
- [Nick Coutsos Keymap Editor](https://nickcoutsos.github.io/keymap-editor/)

The build configuration in this repository already includes the `studio-rpc-usb-uart` snippet required by ZMK Studio.

本仓库的构建配置已经包含 ZMK Studio 所需的 `studio-rpc-usb-uart` snippet。

## Firmware Build / 固件构建

GitHub Actions generates the build matrix from [build.yaml](build.yaml). By default, it builds the following firmware files:

GitHub Actions 会根据 [build.yaml](build.yaml) 生成构建矩阵，默认构建以下固件：

- `felix_left nice_oled`
- `felix_right nice_oled`
- `settings_reset`
- `felix_left nice_view_adapter nice_epaper`
- `felix_right nice_view_adapter nice_epaper`

Before flashing, choose the build artifact that matches your hardware version.

刷写前请根据自己的硬件版本选择对应的构建产物。

## Hardware / 硬件配置

| Item / 项目 | Configuration / 配置 |
| --- | --- |
| Keyboard type / 键盘类型 | Split ortholinear / 分体正交 |
| Layout / 布局 | 5x12+4, 5x6+2 on each side / 5x12+4，左右各 5x6+2 |
| Controller / 主控 | nice!nano / nice!nano v2 |
| Battery / 电池 | 401230 |
| Display / 显示屏 | nice!view / OLED |
| Firmware / 固件 | ZMK |
| Key remapping tools / 改键工具 | ZMK Studio / Nick Coutsos Keymap Editor |

## Credits / 致谢

FelixKeeb is built on the ZMK ecosystem. Thanks to the ZMK project, nice!nano, nice!view, and all open-source hardware and firmware contributors in the community.

FelixKeeb 基于 ZMK 生态构建，感谢 ZMK 项目、nice!nano、nice!view 以及社区中所有开源硬件与固件贡献者。
