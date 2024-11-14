# 编撰说明

## 目标平台

目前版本兼容 FreeBSD 14.1-RELEASE 及 FreeBSD 15.0-CURRENT，并尽量向下兼容。

主要面向 X86、Aarch64 架构，并尽量支持可能多的架构。

Windows 测试环境为 Windows 10、11，并尽量使用最新版本的 Windows。

## pkg 与 ports

因为 FreeBSD 有两种安装软件的方式（但并非所有软件都支持 pkg 的安装方式），因此为了方便，在本跑路教程中已经尽可能地列出了两种方式的安装说明。但希望大家明白，只是为了方便，而并非不能使用 ports 或者 pkg 进行安装或必须使用二者其一进行安装。

> **请注意，ports 一般是 HEAD 分支，你的 pkg 最好与 ports 保持在同一主线上，即都选择 `latest`。**


示例：

要安装软件 `yyy`，`yyy` 在 ports 里是 `xxx/yyy`，即路径是 `/usr/ports/xxx/yyy`。

- 那么首先可以通过 pkg 安装二进制软件包，和绝大多数 Linux 用法一样，下同：

```sh
# pkg install yyy
```

还可以这样：

```sh
# pkg install xxx/yyy
```

或者这样简写：

```sh
# pkg ins yyy
```

- 那么还可以通过 Ports 编译安装：

```sh
# cd /usr/ports/xxx/yyy
# make install clean
```

将会不断地弹出来窗口询问你怎么选。如果是使用默认选项，请这样做，则：

```sh
# cd /usr/ports/xxx/yyy
# make BATCH=yes install clean
```

如果你想一次性完成所有配置：

```sh
# cd /usr/ports/xxx/yyy
# make config-recursive #会一直问你，直到结束依赖
# make install clean
```


## 本书中命令前的符号含义

`#` 代表 `root` 下的操作，基本等同 `sudo`。

`$`、`%` 代表普通用户账户权限。

## 对用户的要求

以高等院校计算机科学与技术学科一般本科毕业生所能达到的及格或及格以上水平为编写难度基准。如未能达到要求，请自行学习。

## 本书定位

本书旨在敉平新手与进阶之间的台阶。
