# RISC-V Toolchains 的国内镜像

克隆 RISC-V GNU Toochain 可能是所有第一次上手 RISC-V 开发的爱好者的第一个坑。由于需要从 GitHub 递归克隆 5GB+ 的仓库，不使用特殊的加速手段的话是很容易劝退新人的。

最近PLCT实验室实习生鈜壬同学和软件所ISRC的佳毅老师合计了一下，整了一个 riscv-toolchains 的国内镜像，主要方便广大国内用户。

顺便希望推广一下ISCAS（中国科学院软件研究所）的 镜像站：国内使用，下载速度贼快，而且 RISC-V 相关资源丰富。如果你需要的资源没有找到，还可以直接在本公众号（RUYISDK）进行留言许愿。

链接在 https://mirror.iscas.ac.cn/riscv-toolchains/

主要分两个部分，一部分是 git 源码，这部分有比如 riscv-gnu-toolchain 这种又大又难 clone 的玩意，也有其他的常用 repo，比如 riscv-isa-manual
另一部分是 release，这里有 riscv spec，还有 pre-built toolchain binary。

这些之前其实 https://mirror.iscas.ac.cn/plct/ 和 https://isrc.iscas.ac.cn/download/riscv/ 在做，不过现在就是有同步脚本可以跟随上游自动更新了。


以下是详细的文档，复制自：
https://mirror.iscas.ac.cn/mirror/riscv-toolchains.html


# RISC-V 工具链镜像使用帮助

本站镜像了 RISC-V 常用工具与文档，分别以 Git 仓库与 Release 的形式镜像

## Git 仓库

本站提供了克隆脚本，以供克隆相关仓库与子模块。样例如下

```
# riscv-gnu-toolchain 及其子模块
## 单独克隆
git clone https://mirror.iscas.ac.cn/riscv-toolchains/git/riscv-collab/riscv-gnu-toolchain.git
## 同时克隆子模块，注意路径为 .git 替换为 .sh
curl https://mirror.iscas.ac.cn/riscv-toolchains/git/riscv-collab/riscv-gnu-toolchain.sh | bash
# rocket-tools 及其子模块
## 单独克隆
git clone https://mirror.iscas.ac.cn/riscv-toolchains/git/chipsalliance/rocket-tools.git
## 同时克隆子模块
curl https://mirror.iscas.ac.cn/riscv-toolchains/git/chipsalliance/rocket-tools.sh | bash
```

已有项目可以在 https://mirror.iscas.ac.cn/riscv-toolchains/git/ 中浏览。

## Release

本站提供了标准文档和预编译工具链的镜像，例如

- RISC-V 非特权与特权指令集文档
- RISC-V 向量扩展指令集文档
- 预编译 riscv-gnu-toolchain

已有项目可以在 https://mirror.iscas.ac.cn/riscv-toolchains/release/ 中浏览。

## 添加镜像

目前该同步脚本（暂时）维护在 https://github.com/tuna/tunasync-scripts/blob/for-iscas/riscv-toolchains.sh 。在后续的维护中，您可以通过 PR 添加新的镜像。
