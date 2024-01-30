# 如意SDK双周进展汇报  第015期·2024年01月30日

## 卷首语

如意SDK V0.4版本今日正式发布。此版本添加了对Allwinner Nezha D1、Sipeed Lichee RV、StarFive VisionFive、StarFive VisionFive2四款RISC-V开发板的支持，包括镜像信息的维护与下载、开发板系统的安装引导，为RISC-V开发者提供了更加便捷的OS获取及安装体验。此外如意软件源新增提供了riscv64 平台的 DynamoRIO 二进制软件包的下载和安装。

随着春节的临近，我们即将迈入2024年。在此，我们先向大家送上春节的祝福，祝大家新春愉快，万事如意！
另外，需要通知各位的是，如意SDK V0.5版本的发布将稍作延迟，调整为2月27日。感谢大家的理解与支持，我们将会带来更多精彩的内容。再次祝大家春节快乐！

## 包管理器

## IDE
IDE部分主要开展了 Eclipse 和 VSCode 对C、Rust、Golang 进行了RISC-V架构上编译和调试现有插件的调研，目前整体来说C、Rust和Golang在RISC-V架构下的交叉编译可走通，但是调试插件还或多或少存在一些问题，缺乏成熟插件甚至无可用调试插件支持。

## GCC


## OpenJDK

OpenJDK RV64 继续持续负责OpenJDK RISC-V相关代码的日常开发、测试、代码检视和架构看护。
1. 两个 OpenJDK LTS (OpenJDK 17.0.10 / OpenJDK 21.0.2) 版本完成 release 发版。
2. 期间向社区提交/检视多个优化的patch, 并排查解决两起社区使用 OpenJDK 相关的问题。

## V8

完成V8 on Android RISC-V的英文文档，并向RISE汇报了此项任务的完成（https://github.com/riscv-collab/v8/wiki/How-to-Run-v8-on-Android-RISCV）。
