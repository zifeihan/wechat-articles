# RuyiSDK双周进展汇报  第018期·2024年03月26日

## 卷首语


## 包管理器


## IDE


## GCC


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


## 操作系统支持矩阵
