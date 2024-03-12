# 如意SDK双周进展汇报  第017期·2024年03月12日

## 卷首语

## 包管理器

## IDE

## GCC

## LLVM

### T-Head Vector 拓展

- 继续完善 LLVM intrinsic 函数，自上次更新以来，新支持了这些类别下的函数：
  - 13.2. Vector Single-Width Averaging Add and Subtract
  - 13.3. Vector Single-Width Fractional Multiply with Rounding and Saturation
- 继续完善 Clang intrinsic 函数，自上次更新以来，新支持了这些类别下的函数：
  - 12.6. Vector Narrowing Integer Right Shift Operations

此外，第一阶段交给上游的 PR 已经提交，正在等待上游的响应。自上次更新以来的进度如下：
- 修复了 llvm-objdump 的操作数输出格式问题
- 将 T-Head Vector 中[新增的汇编指令](https://github.com/T-head-Semi/thead-extension-spec/blob/master/xtheadvector.adoc)与 LLVM MC 合并
- 针对 MC 部分发起对上游的 PR：[[llvm][mc][riscv] MC support of T-Head vector extension (xtheadvector) #84447](https://github.com/llvm/llvm-project/pull/84447)

## OpenJDK

OpenJDK RV64 继续持续负责OpenJDK RISC-V相关代码的日常开发、测试、代码检视和架构看护。

1. Reviewed JDK-mainline PRs:
- https://github.com/openjdk/jdk/pull/17130 (8322179: RISC-V: Implement SHA-1 intrinsic)
- https://github.com/openjdk/jdk/pull/17206 (8322790: RISC-V: Tune costs for shuffles with no conversion)
- https://github.com/openjdk/jdk/pull/17046 (8317721: RISC-V: Implement CRC32 intrinsic)
- https://github.com/openjdk/jdk/pull/17413 (8322174: RISC-V: C2 VectorizedHashCode RVV Version)
- https://github.com/openjdk/jdk/pull/17436 (8323694: RISC-V: Unnecessary ResourceMark in NativeCall::set_destination_mt_safe)
- https://github.com/openjdk/jdk/pull/16989 (8321308: AArch64: Fix matching predication for cbz/cbnz)
- https://github.com/openjdk/jdk/pull/17372 (8323584: AArch64: Unnecessary ResourceMark in NativeCall::set_destination_mt_safe)
- https://github.com/openjdk/jdk/pull/17511 (8324186: AARCH64: Use "dmb.ishst+dmb.ishld" for release barrier)
- https://github.com/openjdk/jdk/pull/17277 (8321137: Reconsider ICStub alignment)
- https://github.com/openjdk/jdk/pull/17450 (JDK-8318228: RISC-V: C2 ConvF2HF)
- https://github.com/openjdk/jdk/pull/17498 (8323748: RISC-V: Add Zfh probe code)
- https://github.com/openjdk/jdk/pull/17519 (8324304: RISC-V: add hw probe flags)
- https://github.com/openjdk/jdk/pull/17513 (8324280: RISC-V: Incorrect implementation in VM_Version::parse_satp_mode)
- https://github.com/openjdk/jdk/pull/17495 (8322630: Remove ICStubs and related safepoints)
- https://github.com/openjdk/jdk/pull/17548 (8324125: Improve class initialization barrier in TemplateTable::_new for RISC-V)
- https://github.com/openjdk/jdk/pull/17646 (8325024: java/security/cert/CertPathValidator/OCSP/OCSPTimeout.java incorrect comment information)

2. Testing before Rampdown/CodeFreeze for LTS versions: OpenJDK 21.0.3 and OpenJDK 17.0.11
- Run OpenJDK tier1-4 regression tests on Unmatched and Licheepi-4A boards.
- Run MineCraft and typical Apache softwares (Netbeans, Lucene, Tomcat, Hadoop, Spark)

3. Co-authored JDK-mainline PRs:

- https://github.com/openjdk/jdk17u-dev/pull/2178 (8324280: RISC-V: Incorrect implementation in VM_Version::parse_satp_mode)
- https://github.com/openjdk/riscv-port-jdk11u/pull/6 (8283929: GHA: Add RISC-V build config)
- https://github.com/openjdk/jdk11u-dev/pull/2549 (8307955: Prefer to PTRACE_GETREGSET instead of PTRACE_GETREGS in method 'ps_proc.c::process_get_lwp_regs')

## V8

## 如意官网

如意官网已于3月1日开启内部测试，官网支持：
* 如意SDK介绍
* 查看支持文档
* 链接社区
* 新闻发布
* 订阅如意SDK newsletter
* 如意SDK下载入口
* 多语言支持
  
