# 功能状态矩阵

随里程碑推进更新。⬜ 未开始 / 🚧 进行中 / ✅ 可用

| 功能 | 状态 | 里程碑 |
|---|---|---|
| 7.3 内核启动 → initramfs shell | ⬜ | M1 |
| 调试通道（ramoops/pstore + USB gadget NCM/ACM） | ⬜ | M1 |
| SSH over USB NCM | ⬜ | M2 |
| Ubuntu Desktop 26.04 rootfs 启动（systemd → login） | ⬜ | M2 |
| 显示（DRM 上屏 → Wayland，llvmpipe） | ⬜ | M3 |
| 触摸（GNOME 交互） | ⬜ | M4 |
| GPU 加速（panthor/panvk 或维持 llvmpipe） | ⬜ | M5 |
| WiFi | ⬜ | M6 |
| 蓝牙 | ⬜ | M6 |
| 电量 / 充电 | ⬜ | M7 |
| thermal / cpufreq | ⬜ | M7 |
| 音频（扬声器 / 耳机 / 内录） | ⬜ | M8 |
| suspend / 亮度 / 音量键 / 传感器 | ⬜ | M9 |
| UART | —（无硬件条件，不规划） | — |
| modem / 相机 / NFC / GNSS | stretch（不在承诺范围） | — |

硬约束常驻：dtbo / 固件分区只读不可刷写；super 不动；_b 槽保留 6.18 oracle。
