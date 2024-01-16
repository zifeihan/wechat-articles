# 如意SDK双周进展汇报  第014期·2024年01月16日

## 卷首语


## 包管理器

项目地址：https://github.com/ruyisdk/ruyi

RuyiSDK 包管理器 `ruyi` 的 0.3.0 版本已于今日发布，您可移步 [GitHub Releases] 或 [ISCAS 镜像源][iscas]下载体验。

[GitHub Releases]: https://github.com/ruyisdk/ruyi/releases/tag/0.3.0
[iscas]: https://mirror.iscas.ac.cn/ruyisdk/ruyi/releases/0.3.0/

本次的更新内容主要有：

* 增加了软件源新闻消息功能。`ruyi update` 后，如有未读的新闻消息，会输出提示信息。
  您可用新增的 `ruyi news list` 与 `ruyi news read` 命令阅读这些消息文章。
* [Issue 32](https://github.com/ruyisdk/ruyi/issues/32)：为 Milk-V Duo、Milk-V Pioneer、Sipeed LicheePi 4A 增加了多种系统镜像，详见 RuyiSDK 官方源的新闻。
  由于这些镜像文件并非都直接由 RuyiSDK 团队打包，当您安装它们时，包管理器将从相应的源站下载：`ruyi` 的版本需要是 0.3.0 或更高。
* 增加了开发板安装器功能：`ruyi device provision`。这是个一步步指导您为手头的 RISC-V 开发板烧写系统镜像、引导器等初始数据的向导。
  初期支持的硬件范围同样是上述 3 种板卡的所有已知不同版本。

欢迎试用或来上游围观；您的需求是我们迭代开发的目标和动力。

## IDE


## GCC
