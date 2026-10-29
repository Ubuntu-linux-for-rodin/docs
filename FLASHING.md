# 刷机指南（骨架，M0 定稿）

## 前置

- 已解锁 bootloader（前置条件，解锁流程不在本项目范围内）
- 宿主机 fastboot（platform-tools）可用

## 槽位

| 槽 | 内容 |
|---|---|
| _a | Ubuntu 试验槽（boot / vendor_boot / vbmeta 自编译产物） |
| _b | 6.18 oracle 槽（对照基线） |

切换：`fastboot set_active a` / `fastboot set_active b`。

## 刷写（Ubuntu 侧）

使用 build 仓脚本（含防误刷 _b 保护）：

```sh
scripts/flash.sh a
```

写入门类仅三个：`boot_${SLOT}` / `vendor_boot_${SLOT}` / `vbmeta_${SLOT}`（`--disable-verity --disable-verification`）。

**绝不刷写 dtbo / 固件分区**——有启动校验，任何情况下不碰。

## 恢复

- 双槽均为自编译内核时，恢复依赖**完整官方 ROM 线刷**——刷写前先验证线刷链路可用
- userdata 被整体写入过，回刷 HyperOS/LineageOS 时数据不保

## TODO(M0)

- vbmeta.img 获取方式固化（官方 ROM 提取 / fastboot fetch）
- fastboot 会话完整示例、常见失败排查
- mkboot.sh 基线参数（页大小 / cmdline / board）从 6.18 刷机流程记录后固化
