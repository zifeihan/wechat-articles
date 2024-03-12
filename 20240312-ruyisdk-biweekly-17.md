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

## V8

## 如意官网
