# 如意SDK双周进展汇报  第016期·2024年02月27日

## 卷首语

## 包管理器

## IDE

## GCC

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

## V8
