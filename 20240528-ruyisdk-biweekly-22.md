# RuyiSDK双周进展汇报  第022期·2024年05月28日

## 卷首语


## 包管理器


## IDE


## GCC


## LLVM

- 继续完善 LLVM intrinsic 函数，自上次更新以来，新支持了这些类别下的函数：
  - 14.7. Vector Floating-Point Square-Root Operations
  - 14.10. Vector Floating-Point MIN/MAX Operations
  - 14.11. Vector Floating-Point Sign-Injection Operations
  - 14.12. Vector Floating-Point Compare Operations
  - 14.13. Vector Floating-Point Classify Operations
  - 14.14. Vector Floating-Point Merge Operations
  - 14.15. Vector Floating-Point Move Operations
  - 14.16. Single-Width Floating-Point/Integer Type-Convert Operations
  - 14.17. Widening Floating-Point/Integer Type-Convert Operations
  - 14.18. Narrowing Floating-Point/Integer Type-Convert Operations
- 完善测试流程和测试数据
  - 增加了 [rvv-intrinsic-doc](https://github.com/riscv-non-isa/rvv-intrinsic-doc) 仓库中位于 `examples/` 目录下的测试用例
  - 在 GitHub Actions 中使用 qemu 6.2 对编译器输出的程序进行模拟运行测试
  - 重新整理 clang 部分对 RVV intrinsic 的测试用例，使其符合用例规范

## OpenJDK


## V8


## 官网


## 操作系统支持矩阵
