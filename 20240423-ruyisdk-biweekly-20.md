# RuyiSDK双周进展汇报  第020期·2024年04月23日

## 卷首语


## 包管理器

RuyiSDK 0.9 对应的包管理器版本也为 0.9.0，已于今日发布。您可移步
[GitHub Releases] 或 [ISCAS 镜像源][iscas]下载体验。

[GitHub Releases]: https://github.com/ruyisdk/ruyi/releases/tag/0.9.0
[iscas]: https://mirror.iscas.ac.cn/ruyisdk/ruyi/releases/0.9.0/

本次 RuyiSDK 包管理器的更新主要包含了以下内容：

* 支持解包 LZ4 格式的压缩文件了。

本次 RuyiSDK 软件源的更新主要包含了以下内容：

* 支持矽速（Sipeed）全线 RISC-V 产品。Ruyi 设备安装器现已新增支持以下设备型号：
    * Sipeed LicheeRV Nano
    * Sipeed Lichee Cluster 4A
    * Sipeed Lichee Console 4A
    * Sipeed Maix-I
    * Sipeed Tang Mega 138K Pro

欢迎试用或来上游围观；您的需求是我们迭代开发的目标和动力。

## IDE


## GCC


## LLVM

### T-Head Vector 拓展

- 继续完善 LLVM intrinsic 函数，自上次更新以来，新支持了这些类别下的函数：
  - 15.1. Vector Single-Width Integer Reduction Operations
  - 15.2. Vector Widening Integer Reduction Operations
  - 15.3. Vector Single-Width Floating-Point Reduction Operations
  - 15.4. Vector Widening Floating-Point Reduction Operations
  - 16.1. Vector Mask-Register Logical Operations
  - 16.2. Vector mask population count vpopc
  - 16.3. vfirst find-first-set mask bit
  - 16.4. vmsbf.m set-before-first mask bit
  - 16.5. vmsif.m set-including-first mask bit
  - 16.6. vmsof.m set-only-first mask bit
  - 16.7. Vector Iota Operations
  - 16.8. Vector Element Index Operations
- 继续完善 Clang intrinsic 函数，自上次更新以来，新支持了这些类别下的函数：
  - 16.1. Vector Mask-Register Logical Operations
  - 16.2. Vector mask population count vpopc
  - 16.3. vfirst find-first-set mask bit
  - 16.4. vmsbf.m set-before-first mask bit
  - 16.5. vmsif.m set-including-first mask bit
  - 16.6. vmsof.m set-only-first mask bit
  - 16.7. Vector Iota Operations
  - 16.8. Vector Element Index Operations

## OpenJDK


## V8


## 官网


## 操作系统支持矩阵
