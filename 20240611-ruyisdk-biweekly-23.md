# RuyiSDK双周进展汇报  第023期·2024年06月11日

## 卷首语

## 包管理器

## IDE

## GCC
支持了Zimop, Zfbfmin等多个新扩展，更新修复了GCC14的部分回归测试问题。

## LLVM

项目大部分 intrinsic 函数已经得到支持，目前正在完善测试流程和测试数据。
至上次更新依赖，新修复了如下问题：

- 修复了 `__riscv_v_elen` 和 `__riscv_v_elen_fp` 在开启 XTHeadVector 拓展时的定义缺失的问题
- 新增加了两个工具内建函数：`vundefined` 和 `vreinterpret`
- 将带 mask 的 RVV intrinsic 函数的 policy 从默认的 TAMA (tail agnostic and masked-off agnostic) 修改为 TAMU (tail agnostic and masked-off undisturbed)，
  使得这些内建函数符合 T-Head Vector 规范。
- 新增了更多测试用例：例如 `rvv_index.c`, `rvv_branch.c` 等。

## V8

## OpenJDK

## 官网

## 操作系统支持矩阵

本周在支持矩阵中新增了更多开发板和操作系统：

- Milk-V Mars: BuildRoot
- Milk-V Duo/Duo S/Duo 256M: Zephyr
- D1: Arch Linux

内容请详见：[ruyisdk/support-matrix](https://github.com/ruyisdk/support-matrix)
