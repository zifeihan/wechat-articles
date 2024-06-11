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
1. Proposed JDK-mainline PRs:
- https://github.com/openjdk/jdk/pull/18716 (8329258: TailCall should not use frame pointer register for jump target)
- https://github.com/openjdk/jdk/pull/19313 (8332533: RISC-V: Enable vector variable shift instructions for machines with RVV)
- https://github.com/openjdk/jdk/pull/19328 (8332615: RISC-V: Support vector unsigned comparison instructions for machines with RVV)
- https://github.com/openjdk/jdk/pull/19415 (8333006: RISC-V: C2: Support vector-scalar and vector-immediate arithmetic instructions)

2. Reviewed JDK-mainline PRs:
- https://github.com/openjdk/jdk/pull/18737 (8330095: RISC-V: Remove obsolete vandn_vi instruction)
- https://github.com/openjdk/jdk/pull/18774 (8330213: RISC-V: C2: assert(false) failed: bad AD file after JDK-8316991)
- https://github.com/openjdk/jdk/pull/18780 (8330242: RISC-V: Simplify and remove CORRECT_COMPILER_ATOMIC_SUPPORT in atomic_linux_riscv.hpp)
- https://github.com/openjdk/jdk/pull/18758 (8330094: RISC-V: Save and restore FRM in the call stub)
- https://github.com/openjdk/jdk/pull/18755 (8330156: RISC-V: Range check auipc + signed 12 imm instruction)
- https://github.com/openjdk/jdk/pull/18785 (8330266: RISC-V: Restore frm to RoundingMode::rne after JNI)
- https://github.com/openjdk/jdk/pull/18875 (8330735: RISC-V: No need to move sp to tmp register in set_last_Java_frame)
- https://github.com/openjdk/jdk/pull/18835 (8321014: RISC-V: C2 VectorLoadShuffle)
- https://github.com/openjdk/jdk/pull/18761 (8330161: RISC-V: Don't use C for Labels jumps)
- https://github.com/openjdk/jdk/pull/18960 (8331150: RISC-V: Fix "bad AD file" bug)
- https://github.com/openjdk/jdk/pull/18477 (8327647: Occasional SIGSEGV in markWord::displaced_mark_helper() for SPECjvm2008 sunflow)
- https://github.com/openjdk/jdk/pull/19448 (8333154: RISC-V: Add support for primitive array C1 clone intrinsic)
- https://github.com/openjdk/jdk/pull/18999 (8331281: RISC-V: C2: Support vector-scalar and vector-immediate bitwise logic instructions)
- https://github.com/openjdk/jdk/pull/19415 (8333006: RISC-V: C2: Support vector-scalar and vector-immediate arithmetic instructions)

## 官网

## 操作系统支持矩阵

本周在支持矩阵中新增了更多开发板和操作系统：

- Milk-V Mars: BuildRoot
- Milk-V Duo/Duo S/Duo 256M: Zephyr
- D1: Arch Linux

内容请详见：[ruyisdk/support-matrix](https://github.com/ruyisdk/support-matrix)
