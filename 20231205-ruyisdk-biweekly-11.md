# 如意SDK双周进展汇报  第011期·2023年12月05日

## 卷首语


## 包管理器

## IDE

IDE 开发者还在招聘中，本期暂无开发进展。



针对Eclipse 对 RISC-V 的现有支持插件进行了一些试用尝试：

- 【完成 & 支持】为 Hello World 工程指定 RISC-V Cross Toolchain 并成功完成交叉编译；

- 【进行中 & 暂未走通】为 Hello World 工程配置 Run Configurations，在Eclipse中集成qemu环境，并完成可执行程序传递、程序执行、执行结果查看；

  > 通过串口设置可以在Eclipse Console中显示qemu加载oerv 23.09 镜像的过程：成功显示了qemu启动oerv23.09 系统过程并显示系统登录提示信息。后续操作需要手动（或者说还未找到更加便捷的方式打通）。
  >
  > qemu user模式设置配置项可能存在问题，未成功在Console中显示打印信息，呈现出预期想要的效果；

- 【进行中 & 暂未走通】为 Hello World 工程配置 Debug Configurations，在qemu中执行交叉调试；

 


## GCC

