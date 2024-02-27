# 如意SDK双周进展汇报  第016期·2024年02月27日

## 卷首语

## 包管理器

## IDE

## GCC

更新了RV64ILP32的[工具链仓库](https://github.com/ruyisdk/riscv-gnu-toolchain-rv64ilp32)，同步更新了各个子模块的实现与构建，补充了中文构建使用说明测试文档

## LLVM

### T-Head Vector 拓展

首先是常规进度更新，如意 SDK 分支中的 T-Head Vector 拓展的进度如下：

- 继续完善 LLVM intrinsic 函数，自上次更新以来，新支持了这些类别下的函数：
  - 12.7. Vector Integer Comparison Operations
  - 12.8. Vector Integer Min/Max Operations
  - 12.9. Vector Single-Width Integer Multiply Operations
  - 12.10. Vector Integer Divide Operations
  - 12.11. Vector Widening Integer Multiply Operations
  - 12.12. Vector Single-Width Integer Multiply-Add Operations
  - 12.13. Vector Widening Integer Multiply-Add Operations
- 继续完善 Clang intrinsic 函数，自上次更新以来，新支持了这些类别下的函数：
  - 12.1. Vector Single-Width Integer Add and Subtract
  - 12.2. Vector Widening Integer Add/Subtract Operations
  - 12.3. Vector Integer Add-with-Carry / Subtract-with-Borrow Operations
  - 12.4. Vector Bitwise Logical Operations
  - 12.5. Vector Single-Width Bit Shift Operations

此外，从年后开始，我们已经开始将如意 SDK 中的 T-Head Vector 拓展的代码与 LLVM 上游仓库合并，
并准备在近期向上游提交 PR。计划中初次 PR 的内容包含如下：

- 注册 T-Head Vector 拓展的名字，版本，依赖拓展，以及对应的拓展冲突检测和相关测试（已完成）
- 包括所有 T-Head Vector 中的汇编指令，即 LLVM MC 支持，以及对应的测试（正在进行）
  - 这部分工作基本以及完成，目前正在进行测试的移植。主要问题为 llvm-objdump 对部分操作数的输出采用了 16 进制格式，但是汇编器的输出是 10 进制格式，导致测试字符串对比不通过。目前正在进行修复。

相关参考链接：https://gcc.gnu.org/pipermail/gcc-patches/2024-January/643490.html

## OpenJDK
OpenJDK RV64 继续持续负责OpenJDK RISC-V相关代码的日常开发、测试、代码检视和架构看护。
1. 完成阿里提交的jdk11u linux-riscv64 代码检视和测试, 目前已经合并到了 riscv-port-jdk11u 仓库
2. 为OpenJDK 主线 linux-riscv64 后端轻量级锁进行了重入锁实现等
3. 检视/测试 OpenJDK 社区关于加解密 intrinsic 的实现等

## V8
