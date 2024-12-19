# 第 4.7 节 安装 Lumina

>**注意**
>
>[Lumina](https://github.com/lumina-desktop/lumina) 在换了开发者后，开发长期处于停滞状态，我向其提交的 pull 长期无人处理，并且没有新的 commit 信息。

## 安装

```sh
# pkg install lumina xorg  lightdm lightdm-gtk-greeter wqy-fonts xdg-user-dirs
```

或者

```sh
# cd /usr/ports/x11/xorg/ && make install clean
# cd /usr/ports/x11/lumina/ && make install clean
# cd /usr/ports/x11-fonts/wqy/ && make install clean
# cd /usr/ports/x11/lightdm/ && make install clean
# cd /usr/ports/x11/lightdm-gtk-greeter/ && make install clean
# cd /usr/ports/devel/xdg-user-dirs/ && make install clean
```

## 配置

```sh
# sysrc dbus_enable="YES"
# sysrc lightdm_enable="YES"
```

```sh
# ee ~/.xinitrc
```

添加：

```sh
exec lumina-desktop
```

## 中文化

> 设置完毕还是英语。原因未知，如果你知道，请提交 issue 或者 pull request。

Desktop Settings ——> Localization ——> 全部调整为“简体中文”，然后“save”，退出登录，重启系统。操作无效。
