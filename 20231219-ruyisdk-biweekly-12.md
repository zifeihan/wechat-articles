# 如意SDK双周进展汇报  第012期·2023年12月19日

## 卷首语

如意SDK V0.2版本发布，为大家提供了一个基础的以编译工具链和模拟器运行环境为主的包管理器，并在12月15日举办的 PLCT Lab OpenDay 2023 线上会议上分享了如意SDK V0.2的建设成果和未来计划，希望这个版本能够给大家带来不一样的编译环境搭建体验，从[文档](https://ruyisdk.github.io/docs/)开始，欢迎大家关注和试用。

## 包管理器

## IDE

本期暂无进展。

## GCC

Bitmanip/Scalar Crypto的intrinsic patch收到了review意见，开发过程中发现了gcc upstream的模板错误，已反馈社区进行了修复。RISC-V Profiles根据review意见重新提交了patch，目前收到新的反馈意见，等待修改后重新发送。修复了OpenHW社区发现的Zca .option段冲突问题，目前已被OpenHW社区合并。Gprofng/libmvec RISC-V后端porting工作持续推进中。
