# 如意SDK双周进展汇报  第017期·2024年03月12日

## 卷首语

如意SDK V0.6 版本如期而至，**[如意SDK官网](https://ruyisdk.org/)上线内测**，网站各基础板块已具备，文档和内容已初步成型。**RISC-V开发板操作系统支持矩阵**一直在持续更新，本期在官网上发布第一版结果。操作系统安装器对已集成的开发板可用操作系统的类型进行了增加。

此外调研了milkv、矽速、沁恒微电子三家厂商的RISC-V产品，开始启动milkv、矽速全产品线支持计划。

更多更新详见下方详情，欢迎大家试用并提供反馈和建议。下一个开发版本 如意SDK V0.7 版本将在 3 月 26 日发布。

## 包管理器

RuyiSDK 0.6 对应的包管理器版本也为 0.6.0，已于今日发布。您可移步
[GitHub Releases][GitHub Releases] 或 [ISCAS 镜像源][iscas]下载体验。

[GitHub Releases]: https://github.com/ruyisdk/ruyi/releases/tag/0.6.0
[iscas]: https://mirror.iscas.ac.cn/ruyisdk/ruyi/releases/0.6.0/

本次更新主要包含了以下内容：

* 不再依赖系统提供的 `git` 命令进行软件源同步了。相应地，您需要确保系统中存在
  TLS 根证书（例如名为 `ca-certificates` 或类似的包），以及 OpenSSL
  库；这对我们官方支持的发行版不是问题。
* `ruyi news` 展示的新闻内容的标题样式更简洁了。

欢迎试用或来上游围观；您的需求是我们迭代开发的目标和动力。

## IDE

本期暂无进展。

## GCC

联合玄铁团队发布了[新32位产品级开源工具链](https://mp.weixin.qq.com/s/argIGP4_rUKDm9IRIB-YTg)，利用64位指令有效减少32位应用的指令数量。
Zabha扩展patch已被上游接受合入,继续推进gprofng与libmvec库的支持中。

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

## 如意官网

如意官网已于3月1日开启内部测试，官网支持：

* 如意SDK介绍
* 查看支持文档
* 链接社区
* 新闻发布
* 订阅如意SDK newsletter
* 如意SDK下载入口
* 多语言支持

官网访问地址：https://ruyisdk.org/

官网仓库：https://github.com/ruyisdk/ruyisdk-website


## 操作系统支持矩阵

RISC-V开发板及其支持的操作系统的支持矩阵公开发布第一版，目前已集成到如意官网。

内容详见：https://github.com/ruyisdk/support-matrix
