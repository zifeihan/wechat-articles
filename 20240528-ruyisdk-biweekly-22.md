# RuyiSDK双周进展汇报  第022期·2024年05月28日

## 卷首语


## 包管理器


## IDE


## GCC


## LLVM

- 继续完善 LLVM intrinsic 函数，自上次更新以来，新支持了这些类别下的函数：
  - 14.7. Vector Floating-Point Square-Root Operations
  - 14.10. Vector Floating-Point MIN/MAX Operations
  - 14.11. Vector Floating-Point Sign-Injection Operations
  - 14.12. Vector Floating-Point Compare Operations
  - 14.13. Vector Floating-Point Classify Operations
  - 14.14. Vector Floating-Point Merge Operations
  - 14.15. Vector Floating-Point Move Operations
  - 14.16. Single-Width Floating-Point/Integer Type-Convert Operations
  - 14.17. Widening Floating-Point/Integer Type-Convert Operations
  - 14.18. Narrowing Floating-Point/Integer Type-Convert Operations
- 完善测试流程和测试数据
  - 增加了 [rvv-intrinsic-doc](https://github.com/riscv-non-isa/rvv-intrinsic-doc) 仓库中位于 `examples/` 目录下的测试用例
  - 在 GitHub Actions 中使用 qemu 6.2 对编译器输出的程序进行模拟运行测试
  - 重新整理 clang 部分对 RVV intrinsic 的测试用例，使其符合用例规范

## OpenJDK
1. Proposed JDK-mainline PRs:
- https://github.com/openjdk/jdk/pull/18716 (8329258: TailCall should not use frame pointer register for jump target)
- https://github.com/openjdk/jdk/pull/18999 (8331281: RISC-V: C2: Support vector-scalar and vector-immediate bitwise logic instructions)
- https://github.com/openjdk/jdk22u/pull/174 (8330094: RISC-V: Save and restore FRM in the call stub)
- https://github.com/openjdk/jdk21u-dev/pull/545 (8330094: RISC-V: Save and restore FRM in the call stub)
- https://github.com/openjdk/jdk17u-dev/pull/2442 (8330094: RISC-V: Save and restore FRM in the call stub)

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


## V8


## 官网

[RuyiSDK 首次线下 Meetup 圆满结束，下次见！](https://mp.weixin.qq.com/s/wHCKdaZLcEyn7CspkIoEmQ)

## 操作系统支持矩阵

本周在支持矩阵中新增了更多开发板和操作系统：

- R128
- BeagleV-Ahead
- BeagleV-Fire
- Star64
- MongoPi MQ Pro
- Duo 256M
- BPi-F3
- DongshanPI-哪吒 STU
- DongshanPI D1s
- D1s NeZha
- Mangopi MQ
- CH573
- Polarfire SoC FPGA Icicle Kit

内容请详见：[ruyisdk/support-matrix](https://github.com/ruyisdk/support-matrix)

至此，操作系统支持矩阵已覆盖了超过 50 款开发板，撒花~
