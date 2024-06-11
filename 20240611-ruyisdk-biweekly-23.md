# RuyiSDK双周进展汇报  第023期·2024年06月11日

## 卷首语

## 包管理器

RuyiSDK 0.12 对应的包管理器版本也为 0.12.0，已于今日发布。您可移步
[GitHub Releases] 或 [ISCAS 镜像源][iscas]下载体验。

[GitHub Releases]: https://github.com/ruyisdk/ruyi/releases/tag/0.12.0
[iscas]: https://mirror.iscas.ac.cn/ruyisdk/ruyi/releases/0.12.0/

本次 RuyiSDK 包管理器的更新主要包含了以下内容：

* 修复了先前 Pine64 Star64 Armbian 镜像无法下载的问题。
* 对于部分必须由用户手工下载的文件，支持了相应的用户体验：按照当前系统语言设置，渲染相应的提示语。
* 升级了 pygit2 依赖库版本到 1.5.0，以支持 libgit2 的 1.8 版本。
* 修复了 `XDG_STATE_HOME` 环境变量被无视的问题。

为了支持刷写方式复杂、需要夹杂人工干预、镜像文件需要手工下载等复杂情况下的设备初始化，我们正在对设备安装器进行重构，预计将于下个版本付诸测试。届时旧版
`ruyi` 的设备安装器功能将不可用，请先升级再进行体验。

欢迎试用或来上游围观；您的需求是我们迭代开发的目标和动力。

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
