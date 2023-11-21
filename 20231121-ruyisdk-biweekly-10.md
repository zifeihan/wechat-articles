# 如意SDK双周进展汇报  第010期·2023年11月21日

## 卷首语

## 包管理器

需求变更：ruyi v0.2 新增了 sysroot、QEMU 的支持需求，该版本的代码冻结因而未在上周完成。
目前仍然在做 QEMU、LLVM 的打包工作。

完成了从上游源码、平头哥源码构建的 GCC 工具链的打包，期间修复了上游 crosstool-ng 的 [multilib 构建问题一处](https://github.com/xen0n/crosstool-ng/commit/12db6b2d83fe9deec1607813a63ee92e135a93c9)，待提交上游。

为方便未及时升级系统的同学们测试、使用，现已将工具链、`ruyi` 二进制的构建容器系统版本降低到了 Ubuntu 20.04。
但 `ruyi` 官方支持的系统版本基线维持不变：仍然为 Ubuntu 22.04、openEuler 23.09。

此外，对如意软件源结构做了一些更新，详见[文档](https://github.com/ruyisdk/ruyi/blob/main/docs/repo-structure.md)：

* 为使 repo 内的软件包信息有条理，新增了软件包分类的概念，将原先扁平的目录结构加深 1 层；
* 为方便后续迭代、表达特殊语义等需要，预留了下划线开头的包名，后续再行 case-by-case 定义。

## IDE

## GCC
