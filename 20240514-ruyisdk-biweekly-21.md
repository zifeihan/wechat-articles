# RuyiSDK双周进展汇报  第021期·2024年05月14日

## 卷首语

## 包管理器

## IDE

## GCC
更新了RUYISDK GCC14分支，目前正在rebase rv64ilp32/SIMD/Profiles等特性中。

## LLVM

- 增加针对 T-Head Vector 的优化 Pass
  - 增加了 `RedundantVSETVLIElimination` 优化过程，用于消除冗余的 `vsetvli` 指令

- 继续完善 LLVM intrinsic 函数，自上次更新以来，新支持了这些类别下的函数：
  - 14.1. Vector Single-Width Floating-Point Add/Subtract Operations
  - 14.2. Vector Widening Floating-Point Add/Subtract Operations
  - 14.3. Vector Single-Width Floating-Point Multiply/Divide Operations
  - 14.4. Vector Widening Floating-Point Multiply Operations
  - 14.5. Vector Single-Width Floating-Point Fused Multiply-Add Operations
  - 14.6. Vector Widening Floating-Point Fused Multiply-Add Operations
  - 14.7. Vector Floating-Point Square-Root Operations
  - 14.8. Vector Floating-Point Reciprocal Square-Root Estimate Operations
  - 14.9. Vector Floating-Point Reciprocal Estimate Operations
  - 14.10. Vector Floating-Point MIN/MAX Operations
  - 14.11. Vector Floating-Point Sign-Injection Operations
  - 14.12. Vector Floating-Point Compare Operations
  - 14.13. Vector Floating-Point Classify Operations
  - 14.14. Vector Floating-Point Merge Operations
  - 14.15. Vector Floating-Point Move Operations
  - 14.16. Single-Width Floating-Point/Integer Type-Convert Operations
  - 14.17. Widening Floating-Point/Integer Type-Convert Operations
  - 14.18. Narrowing Floating-Point/Integer Type-Convert Operations
  - 17.2. Integer Scalar Move Operations
  - 17.3. Floating-Point Scalar Move Operations
  - 17.4. Vector Slide Operations
  - 17.5. Vector Register Gather Operations
  - 17.6. Vector Compress Operations
- 继续完善 Clang intrinsic 函数，自上次更新以来，新支持了这些类别下的函数：
  - 14.1. Vector Single-Width Floating-Point Add/Subtract Operations
  - 14.2. Vector Widening Floating-Point Add/Subtract Operations
  - 14.3. Vector Single-Width Floating-Point Multiply/Divide Operations
  - 14.4. Vector Widening Floating-Point Multiply Operations
  - 14.5. Vector Single-Width Floating-Point Fused Multiply-Add Operations
  - 14.6. Vector Widening Floating-Point Fused Multiply-Add Operations
  - 15.1. Vector Single-Width Integer Reduction Operations
  - 15.2. Vector Widening Integer Reduction Operations
  - 15.3. Vector Single-Width Floating-Point Reduction Operations
  - 15.4. Vector Widening Floating-Point Reduction Operations
  - 17.4. Vector Slide Operations
  - 17.5. Vector Register Gather Operations
  - 17.6. Vector Compress Operations

## OpenJDK

## V8

## 官网

## 操作系统支持矩阵

新增部分全志、芯来开发板的系统支持情况调研；基于现有开发板和相关文档展开测试验证，产出测试报告。

- Milk-V Duo S 
    - NuttX
        - 新版本重新测试
    - BuildRoot
    - Debian
- CanMV / Kendryte K230
    - NuttX
    - RT-Thread
- StarFive VisionFive 2
    - NuttX
- Maix-I K210
    - NuttX
- Nuclei DDR200T
    - FreeRTOS
    - RT-Thread
- Longan Nano
    - RT-Thread
- RV Star
    - FreeRTOS
    - RT-Thread
- 100ASK-V853-PRO (Allwinner V853)
    - Melis
- CM32M433R-START
    - FreeRTOS
    - RT-Thread
- TinyVision
    - Melis
- Allwinner V853
    - Melis
- Youmu Pi
    - Melis

内容请详见：[ruyisdk/support-matrix](https://github.com/ruyisdk/support-matrix)
