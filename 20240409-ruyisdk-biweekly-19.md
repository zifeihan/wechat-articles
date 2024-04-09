# RuyiSDK双周进展汇报  第019期·2024年04月09日

## 卷首语


## 包管理器


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
