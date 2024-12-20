# 第 4.4 节 安装 Mate

> 以下教程适用于 shell 为 bash/sh/zsh 的用户。
>
> 首先看看现在自己的 shell 是不是 `sh`、`bash` 或 `zsh`：
>
>```sh
># echo $0
>```
>
> 如果是 `sh`、`bash`、`zsh` 其中之一，请继续；

## 安装与配置

```sh
# pkg install  mate xorg wqy-fonts lightdm lightdm-gtk-greeter xdg-user-dirs
```

或者：

```sh
# cd /usr/ports/x11/mate/ && make install clean
# cd /usr/ports/x11/xorg/ && make install clean
# cd /usr/ports/x11-fonts/wqy/ && make install clean
# cd /usr/ports/x11/lightdm-gtk-greeter/ && make install clean
# cd /usr/ports/devel/xdg-user-dirs/ && make install clean
```

安装后启动服务：

```sh
# sysrc moused_enable="YES"
# sysrc dbus_enable="YES"
# sysrc lightdm_enable="YES"
```

- 在主目录`.xinitrc` 文件内加入下面一行:

```
exec mate-session
```

## 显示中文桌面环境

默认是 csh，在 `~/.cshrc` 中添加如下内容：

```sh
setenv LANG zh_CN.UTF-8
setenv LC_CTYPE zh_CN.UTF-8
```

## 输入法

```sh
# pkg install zh-ibus-libpinyin
```

或者:

```sh
# cd /usr/ports/chinese/ibus-libpinyin/ 
# make install clean
```

安装好运行初始化命令 `ibus-setup`。

设置输入法变量:

```sh
# ee ~/.xinitrc
```

在该文件中添加以下内容

```sh
export GTK_IM_MODULE=ibus
export XMODIFIERS=@im=ibus
export QT_IM_MODULE=ibus
ibus &
```
