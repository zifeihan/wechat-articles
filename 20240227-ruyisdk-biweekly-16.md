# 如意SDK双周进展汇报  第016期·2024年02月27日

## 卷首语

如意SDK V0.5 版本如期发布，此版本集成并发布了 PLCT GNU 小队新发布的 GNU RV64ILP32 工具链，并更新了适用 th1520 的 plctxthead-linux-gnu 工具链。继续扩展了系统安装器支持的 RISC-V 开发板，添加了对 SiFive HiFive Unmatched 、Canaan Kendryte K230  两款RISC-V 开发板的支持，包括镜像信息的维护与下载、开发板系统的安装引导。

更多更新详见下方详情，欢迎大家试用并提供反馈和建议。下一个开发版本 如意SDK V0.6 版本将在 3 月 12 日发布。

## 包管理器

## IDE

IDE部分主要开展了 Dart 、Chisel RISC-V架构上编译和调试现有插件的调研。Dart 目前可以借助 JIT 或 AOT 在 linux 系统本机编译或运行 RISC-V 目标的程序 (实验性)，不能在本机进行交叉编译 (除 flutter)。

Chisel所需的 Verilog仿真器 Verilator 目前在部分Linux（如openEuler）发行版支持还需完善，此外运行过程中遇到一些问题还在继续了解中。Chisel 对 RISC-V 项目的支持目前比较普及，国内很多RISC-V处理器设计相关项目均采用的Chisel，如香山。

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

1. 向V8上游提交了RISCV64 Android构建的支持，已合并；
2. 实现了WebAssembly的新特性 Out of Bounds Trap Handling 在RISC-V后端的支持。
