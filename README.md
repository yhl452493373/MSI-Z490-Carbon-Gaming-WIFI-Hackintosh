# MSI-Z490-Carbon-Gaming-WIFI-Hackintosh

### EFI of MSI Z490 Carbon Gaming WIFI Hackintosh with OpenCore

- 2021.12.17 修复唤醒后进入睡眠，会被 XDCI 设备间歇唤醒问题
- 2021.12.15 修复睡眠后 2 小时会被 RTC 唤醒一次的问题
- 2021.12.12 初次提交，OpenCore 版本为 0.76，测试系统为 macOS Monterey 12.0.1 (21A559)

---

| 配置        | 规格                         |
| ----------- | ---------------------------- |
| 主板        | 微星 Z490 Carbon Gaming WIFI |
| CPU         | i7 10700K                    |
| 内存        | 玖合 DDR4 3200 16G x 2       |
| 显示器      | 联合创新 27C1U 4K/60Hz       |
| WIFI 和蓝牙 | DW1560                       |
| 硬盘        | 阿斯加特 2TB NVME            |
| 显卡        | CPU 集成显卡 UHD 630         |
| BIOS 版本   | E7C731MS.1A0                 |

---

| 关注项                     | 工作情况 | 特殊说明                                                                                                                                                   |
| -------------------------- | -------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 单 DP 输出                 | 正常     |                                                                                                                                                            |
| 单 HDMI 输出               | 正常     | 主板限制，HDMI 为 1.4，只能输出 4K 30Hz                                                                                                                    |
| DP 和 HDMI 同时输出        | 正常     | 同时插上开机，则只有 HDMI 有输出，需要把 HDMI 重新插拔一次，DP 才有输出                                                                                    |
| 板载声卡和显示器音频输出   | 正常     |                                                                                                                                                            |
| WIFI 和蓝牙                | 正常     | 自带的 AX201 在 macOS 下不好用，其蓝牙端口屏蔽，macOS 下用 DW1560 代替                                                                                     |
| 板载 2.5G 网卡             | 正常     |                                                                                                                                                            |
| 睡眠和唤醒（支持键鼠唤醒） | 正常     | 关闭节能中的“唤醒以供网络访问”、“断电后自动启动”、“启用电能小憩”                                                                                           |
| 关机                       | 正常     |                                                                                                                                                            |
| 重启                       | 正常     |                                                                                                                                                            |
| USB 端口定制               | 正常     | 只定制了所有的 USB3.0 Type-A 和 Type-C 端口，自带的 USB2.0 Type-A 屏蔽；前置 USB3.0 均定制；前置 USB2.0 接口只定制了靠近声卡的接口，用于连接 DW1560 的蓝牙 |
| 前置耳机、麦克风接口       | 正常     |                                                                                                                                                            |

---

| BIOS 项                   | 状态 |
| ------------------------- | ---- |
| CFG 锁定                  | 禁止 |
| USB 设备从 S3/S4/S5 唤醒  | 允许 |
| 集成显卡多显示器          | 允许 |
| SW Guard Extensions (SGX) | 禁止 |
| 快速开机                  | 禁止 |
| Re-Size BAR Support       | 允许 |
| 串口配置 -> 串口 0        | 禁止 |
| 集显共享内存              | 64MB |

---

| macOS 系统偏好设置项                   | 状态     |
| -------------------------------------- | -------- |
| 唤醒以供以网络访问                     | 取消勾选 |
| 断电后自动启动                         | 取消勾选 |
| 启用电能小憩                           | 取消勾选 |
