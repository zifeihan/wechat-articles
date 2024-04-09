# RuyiSDK双周进展汇报  第019期·2024年04月09日

## 卷首语


## 包管理器

RuyiSDK 0.8 对应的包管理器版本也为 0.8.0，已于今日发布。您可移步
[GitHub Releases] 或 [ISCAS 镜像源][iscas]下载体验。

[GitHub Releases]: https://github.com/ruyisdk/ruyi/releases/tag/0.8.0
[iscas]: https://mirror.iscas.ac.cn/ruyisdk/ruyi/releases/0.8.0/

本次 RuyiSDK 包管理器的更新主要包含了以下内容：

* 默认禁止了以 `root` 身份运行 `ruyi`，以提升安全性。如确有需要，可按程序提示设置环境变量以绕过检查，但我们不推荐这么做。
* 迭代了软件源格式：
    * 支持以 TOML 格式撰写软件源全局配置及包定义文件。相比先前采用的 JSON 格式，更便于手工编辑、添加注释、标记文件格式版本等，有利于维护。
    * 支持定义上游镜像了。后续对那些本身也通过镜像分发的软件包，也能借助此功能，利用上它们的镜像了，有利于提高用户一侧的下载速度与可靠性。
* 支持在 `wget` 与 `curl` 均不可用的系统上下载文件了。
* 安装软件包时的解包操作现在具备原子性了。这意味着一旦解包被中断，重试时，`ruyi` 不会错误以为该包已经安装完成了。
* 持续优化工程实践：
    * 目前所有代码贡献都会在代码风格、类型注解、开源许可证遵守方面接受检查了。
    * 改进了打包流程，使 `ruyi` 官方二进制的包体得到了一定的瘦身。

欢迎试用或来上游围观；您的需求是我们迭代开发的目标和动力。

## IDE


## GCC


## LLVM

### T-Head Vector 拓展

- 继续完善 LLVM intrinsic 函数，自上次更新以来，新支持了这些类别下的函数：
  - 14.1. Vector Single-Width Floating-Point Add/Subtract Operations
  - 14.3. Vector Single-Width Floating-Point Multiply/Divide Operations
- 继续完善 Clang intrinsic 函数，自上次更新以来，新支持了这些类别下的函数：
  - 13.1. Vector Single-Width Saturating Add and Subtract
  - 13.5. Vector Narrowing Fixed-Point Clip Operations

此外，本次将 T-Head Vector 分支 rebase 到了 LLVM 17.0.6 版本。

## OpenJDK


## 官网


## 操作系统支持矩阵

完成了对绝大多数市面常见 RISC-V 开发板操作系统支持情况的调研，并编写了测试报告。新增了对 Lichee Cluster 4A、Lichee Console 4A、Sipeed Maix-I、Lichee RV Nano 的系统支持情况调研。

内容详见：https://github.com/ruyisdk/support-matrix
