# Ubuntu for Rodin — 文档仓

把 **Ubuntu Desktop 26.04 LTS** 完整带到 **Redmi Turbo 4（国行）/ POCO X7 Pro**（代号 **rodin**，MT6899 天玑 8400-Ultra）上：上游 Linux 内核 + 原生 systemd/GNOME 用户态，不依赖 Android 框架。

项目路线图即项目 README 全文，以 org 主 README 为单一来源维护。本仓收录配套文档：

- [FLASHING.md](FLASHING.md) — 刷机指南（骨架）
- [STATUS.md](STATUS.md) — 功能状态矩阵

## 仓库导航

| 仓库 | 内容 |
|---|---|
| [`linux`](https://github.com/Ubuntu-linux-for-rodin/linux) | v7.3 上游基线 + rodin 前向移植 |
| [`initramfs`](https://github.com/Ubuntu-linux-for-rodin/initramfs) | stage-1（挂根 / rescue） |
| `build` | 镜像组包 / fastboot 刷写脚本 |
| `rootfs` | Ubuntu Desktop rootfs 构建器 + 固件提取 |
| `docs` | 本仓 |

## 硬约束（全项目通用）

- **dtbo / 固件分区只读不可刷写**（有启动校验）
- super 不动；userdata 独占作 Ubuntu rootfs
- _a = Ubuntu 试验槽，_b = 6.18 oracle 槽
