# RuyiSDK双周进展汇报  第018期·2024年03月26日

## 卷首语

RuyiSDK V0.7 版本今日正式发布。**GCC上游社区合并了PLCT提交的香山南湖微架构补丁**，RuyiSDK包管理器正在对最新的gnu-upstream进行新版本的打包分发，预计近日将发布；RuyiSDK **官网已公开内测**；操作系统安装器新增了Milk-V Duo S、Milk-V Mars、Milk-V Vega等产品的集成，截止本版本为止，**Milk-V当前全产品线已经初步集成到RuyiSDK包管理器**（Milk-V Duo S、Milk-V Mars 设备暂时未到位测试验证后续补充，欢迎有设备的开发者们试用反馈）。

更多更新详见下方详情，欢迎大家试用并提供反馈和建议。下一个开发版本 RuyiSDK V0.8 版本将在 4 月 9 日发布。

## 包管理器

## IDE

集成开发环境 VSCode开发部分目前征集到一位内部兼职开发者，开始尝试基于VSCode实现 Milkv 开发板的集成开发工作。

## GCC

香山南湖的微架构支持已合入GCC上游，继续推进RUYISDK多版本GCC的支持工作，更新了“-march=help”特性的支持。

## LLVM

### T-Head Vector 拓展

- 继续完善 LLVM intrinsic 函数，自上次更新以来，新支持了这些类别下的函数：
  - 13.1. Vector Single-Width Saturating Add and Subtract
  - 13.5. Vector Narrowing Fixed-Point Clip Operations
- 继续完善 Clang intrinsic 函数，自上次更新以来，新支持了这些类别下的函数：
  - 12.7. Vector Integer Comparison Operations
  - 12.8. Vector Integer Min/Max Operations
  - 12.9. Vector Single-Width Integer Multiply Operations
  - 12.10. Vector Integer Divide Operations
  - 12.11. Vector Widening Integer Multiply Operations
  - 12.12. Vector Single-Width Integer Multiply-Add Operations
  - 12.13. Vector Widening Integer Multiply-Add Operations
  - 12.14. Vector Integer Merge Operations
  - 13.3. Vector Single-Width Fractional Multiply with Rounding and Saturation

## OpenJDK

OpenJDK RV64 继续持续负责OpenJDK RISC-V相关代码的日常开发、测试、代码检视和架构看护。

1. Reviewed JDK-mainline PRs:

- https://github.com/openjdk/jdk/pull/17698 (8320646: RISC-V: C2 VectorCastHF2F)
- https://github.com/openjdk/jdk/pull/17820 (8321282: RISC-V: SpinPause() not implemented)
- https://github.com/openjdk/jdk/pull/17889 (8321075: RISC-V: UseSystemMemoryBarrier lacking proper OS support)
- https://github.com/openjdk/jdk/pull/17924 (8326235: RISC-V: Size CodeCache for short calls encoding)
- https://github.com/openjdk/jdk/pull/17750 (8324124: RISC-V: implement _vectorizedMismatch intrinsic)
- https://github.com/openjdk/jdk/pull/17964 (8322962: Upcall stub might go undetected when freezing frames)
- https://github.com/openjdk/jdk/pull/17554 (8319900: Recursive lightweight locking: riscv64 implementation)
- https://github.com/openjdk/jdk/pull/18039 (8326936: RISC-V: Shenandoah GC crashes due to incorrect atomic memory operations)

2. Reviewed JDK21u upstream PRs:

- https://github.com/openjdk/jdk21u-dev/pull/294 (8321075: RISC-V: UseSystemMemoryBarrier lacking proper OS support)

3. Reviewed JDK11u upstream PRs:

- https://github.com/openjdk/jdk11u-dev/pull/2549 (8307955: Prefer to PTRACE_GETREGSET instead of PTRACE_GETREGS in method 'ps_proc.c::process_get_lwp_regs')

4. Reviewed riscv-port-jdk11u backport PRs:

- https://github.com/openjdk/riscv-port-jdk11u/pull/6 (8283929: GHA: Add RISC-V build config
  8313701: GHA: RISC-V should use the official repository for bootstrap
  8285630: Fix a configure error in RISC-V cross build)
- https://github.com/openjdk/riscv-port-jdk11u/pull/7 (8290496: riscv: Fix build warnings-as-errors with GCC 11)
- https://github.com/openjdk/riscv-port-jdk11u/pull/9 (JDK-8327284: Use correct register in riscv_enc_fast_unlock())
- https://github.com/openjdk/riscv-port-jdk11u/pull/10 (8316645: RISC-V: Remove dependency on libatomic by adding cmpxchg 1b)

5. riscv-port-jdk11u daily build available at: https://builds.shipilev.net/openjdk-jdk11-riscv/
6. Troubleshoot GHA linux-cross-build (linux-riscv64) failure (https://bugs.openjdk.org/browse/JDK-8326960 )
7. OpenJDK PRs

- https://github.com/openjdk/jdk/pull/18114 (8327283: RISC-V: Minimal build failed after JDK-8319716)
- https://github.com/openjdk/jdk/pull/18131 (8327426: RISC-V: Move alignment shim into initialize_header() in C1_MacroAssembler::allocate_array)
- https://github.com/openjdk/jdk/pull/18175 (8327716: RISC-V: Change type of vector_length param of several assembler functions from int to uint)
- https://github.com/openjdk/jdk22u/pull/90 (8326936: RISC-V: Shenandoah GC crashes due to incorrect atomic memory operations)
- https://github.com/openjdk/riscv-port-jdk11u/pull/7 (8290496: riscv: Fix build warnings-as-errors with GCC 11)

## 官网

官网访问地址：https://ruyisdk.org/

官网仓库：https://github.com/ruyisdk/ruyisdk-website

官网近期完成了细节的更新、文档更新、i18n多语言支持相关的工作。目前公开[邀请测试](https://mp.weixin.qq.com/s/p3WmhN27aAaMPlL4vP39IQ)中。

## 操作系统支持矩阵

对RISC-V开发板及其支持的操作系统的支持矩阵的内容和文档进行了更新和完善，并增加了Milk-V Duo S、Milk-V Mars、Milk-V Vega等新设备的支持调研，Milk-V Duo S、Milk-V Mars在开发板上的实际测试验证等待采购设备到位后开展。

内容详见：https://github.com/ruyisdk/support-matrix
