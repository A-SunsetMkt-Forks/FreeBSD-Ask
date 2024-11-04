# FreeBSD 从入门到跑路

~~为了拯救即将归档（Archived）的 FreeBSD.....我们决定写一本书~~

## 贡献指南

如果你想让你的教程出现在本书中，你可以这样做：

- 如果你熟悉 GitHub，可以点击电脑端右侧的“编辑此页”，进入项目进行操作。整个项目使用 Markdown 语法 +  Gitbook，简单易上手（具体详见项目 WiKi）；
- 如果以上有困难，你还可以发 PDF、Word 或者 TXT 给我。请将文件发送至电子邮件 `yklaxds@gmail.com`；如果有视频教程，以各大云盘链接为宜。

本书现接受以下内容：

- 一切与 BSD 相关（包括不限于 FreeBSD，OpenBSD，NetBSD）以及各种体系结构的教程。你既可以扩充当前教程，也可以新建一节；
- 下方的 ToDo 列表；
- 你亦可在文学故事章节分享你与 BSD 的故事，你的个人心得体会。

你为什么要这样做？

- **可访问性**：随处可见，无需再到处寻找；
- **可复现性**：任何人都能轻松复现成果，显著提高工作和学习效率；
- **规模化测试**：可以对教程进行系统化测试，找出最优解；
- **社区支持**：社区将持续维护教程的可用性，并定期更新软件和教程版本；
- **节省时间**：当本教程内容愈加丰富，你花在网络索引上的无效时间就会越少；
- **互惠互利**：合并教程践行了开源哲学，惠及着无穷的远方，无数的人们；
- **增强协作**：促进 FreeBSD 在中国乃至亚洲、全世界的发展；
- **便于反馈**：快速迭代教程，并验证每一步骤的正确性与合理性；
- **易于分享**：本项目既支持在线浏览亦支持 PDF 文档导出，宽松的许可证、简单的项目结构允许自由部署。

唯一要注意的是，你的教程会以本项目的开源许可证（BSD）进行发布。

### 意见反馈

由于编写者水平所限，书中缺点和谬误之处自不可免，希望大家随时提出批评意见，以便修正。你可以利用 Github 提交 Issue 或者发邮件至 `yklaxds@gmail.com`。

## 现成的虚拟机镜像体验（本书自制）

具体详情请参见第 2 章节。

```json
14.1  磁力链接  magnet:?xt=urn:btih:496C343387D74457E441CAFA93B302E791F62924

15.0  磁力链接  magnet:?xt=urn:btih:CBD49C71E87BC0B1406710A437E7135EF3D8C155
```
## ToDo


- [ ] 整合现有的上游 FreeBSD 社区文章
- [ ] 重写“第 4.1 节 安装显卡驱动及 Xorg（必看）”，尤其是 N 卡驱动部分，目前是无效的，必须重写
- [ ] `pkg autoremove`（会把整个系统都带走）及 `pkg delete`（破坏依赖）都不是正经的卸载软件及孤包依赖的方法，`pkg-rmleaf` 亦已过时无法使用。需要找到正常合理的卸载软件包的方法。`pkg_rmleaves` 似乎可以
- [X] 补充一些 WinSCP、XShell 的替代工具，避免单一来源
  - [ ] 找到一款我认为能替代二者的工具
- [X] 将全书主观性文字转换为思考题供读者自行思考与判断
- [ ] 更新“第 16.7 节 Samba 服务器”
- [ ] 删除重写部分来源于网络的错误内容
  - [ ] 防火墙
  - [ ] jail
  - [ ] 用户与权限
  - [ ] geom 合并到第 6 章
  - [ ] 删除无实际内容的 DTrace 章节
- [ ] 完全面向新手介绍 FreeBSD
  - [ ] 对比 Linux、Windows、MacOS、Android 和 IOS 等常见操作系统
  - [ ] 客观化论证
    - [ ] 删除冗余，精简论证
    - [X] 补充参考文献
    - [ ] 客观陈述不足，面对现实
- [X] 重写第一章，考虑加入硬件常识，整合现有的树莓派章节相关内容
- [ ] 文学故事章节需要重写
  - [ ] 说明真实看法，避免曲解和误导，旨在强调对 Linux 和开源没有恶意
  - [ ] 删除冗余，精简论证
  - [ ] 客观化
    - [ ] 名人名言
    - [ ] 图片
    - [ ] 视频
    - [X] 参考文献
    - [ ] 说明各大 Linux 操作系统的优势
- [ ] 补充一些实验
  - [ ] 我的世界（服务器、客户端）
- [ ] ZFS（可以参考 [Oracle Solaris 管理：ZFS 文件系统](https://docs.oracle.com/cd/E26926_01/html/E25826/index.html)）
  - [ ] ZFS 共享
  - [ ] ZFS 加密
  - [ ] ZFS 调优
  - [ ] ZFS iSCSI
  - [ ] 补充 ZFS 委托管理
  - [ ] 归档快照和根池恢复
  - [ ] ZFS 故障排除
  - [ ] ZFS 克隆
  - [ ] ZFS 与 ACL
  - [ ] ZFS 高级主题
  - [ ] ZFS 池管理
  - [ ] ZFS 与 RAID
- [X] 将小说诗歌杂记等与 FreeBSD 无关内容下线
- [ ] 参照 FreeBSD handbook、鸟哥的 Linux 私房菜服务器篇改写服务器相关章节
  - [ ] BSD 常用网络命令
  - [ ] 链路聚合
  - [ ] IPv6 配置
    - [ ] WiFi
    - [ ] 以太网
  - [ ] DNS
  - [ ] DHCP
  - [ ] 更新：第 17.8 节 PostgreSQL 与 pgAdmin4
  - [ ] NTP
  - [ ] NFS
  - [ ] iSCSI
  - [ ] Postfix
  - [ ] LDAP（OpenLDAP，也许可以参考 [WiKi LDAP/Setup](https://wiki.freebsd.org/LDAP/Setup)）
- [X] NextCloud（最好基于 PostgreSQL）
- [ ] KDE6
  - [ ] 基于 Xorg
  - [ ] 基于 Wayland
- [ ] Wayland
  - [ ] 远程软件
  - [ ] 桌面
- [ ] FreeBSD 路由器
- [ ] Wine
  - [ ] 填充实质性内容
  - [ ] 64 位 Windows 程序（64 位 Wine？）
- [ ] FreeBSD 安全加固（可参照 [FreeBSD 14 CIS 基准](https://www.cisecurity.org/cis-benchmarks)，[阿里云盘](https://www.alipan.com/s/9Vced5R3Wit)）
  - [ ] 云服务器
  - [ ] 路由器
  - [ ] 小主机
  - [ ] 桌面用户
  - [ ] 虚拟机
  - [ ] 限制端口
  - [ ] 防火墙
- [ ] 微信

---

- [ ] OpenBSD
  - [ ] KDE5（现在进入桌面黑屏）
  - [ ] OpenBSD 调优
  - [ ] OpenBSD 安全加固
  - [ ] 网络
    - [ ] DNS
    - [ ] FTP
    - [ ] NTP
    - [ ] DHCP
    - [ ] 各式代理
    - [ ] 邮件服务器
    - [ ] PF 等防火墙
    - [ ] IPv6
    - [ ] 常用网络命令
  - [ ] OpenBSD 路由器（可参考 [OpenBSD 路由器指南](https://translated-articles.bsdcn.org/2023-nian-9-yue/openbsd-router-guide)）
    - [ ] WiFi
    - [ ] 链路聚合
    - [ ] 路由表
    - [ ] 默认路由
  - [ ] OpenBSD 基础知识
    - [ ] 版本概况
    - [ ] 开发宗旨与项目目标
    - [ ] 性能参数
    - [ ] 注意事项
    - [ ] 跟踪新版本
    - [ ] pkgsrc
  - [ ] 嵌入式

---

- [ ] NetBSD
  - [ ] NetBSD 调优
  - [ ] 桌面
    - [ ] 火狐浏览器
    - [ ] Chromium
    - [ ] KDE 4（现在进入桌面黑屏）
  - [ ] 树莓派 4 & 5
  - [ ] NetBSD 安全加固
  - [ ] NetBSD 基础知识
    - [ ] 版本概况
    - [ ] 开发宗旨与项目目标
    - [ ] 注意事项
    - [ ] 跟踪新版本
    - [ ] pkgsrc
  - [ ] 嵌入式  
  - [ ] 网络
    - [ ] DNS
    - [ ] FTP
    - [ ] NTP
    - [ ] DHCP
    - [ ] 各式代理
    - [ ] 邮件服务器
    - [ ] PF 等防火墙
    - [ ] IPv6
    - [ ] 常用网络命令
  - [ ] OpenBSD 路由器
    - [ ] WiFi
    - [ ] 链路聚合
    - [ ] 路由表
    - [ ] 默认路由

---
       
      
- [ ] DragonFlyBSD
  - [ ] DragonFlyBSD调优
  - [ ] 桌面
    - [ ] KDE5
    - [ ] Gnome
    - [ ] XFCE
    - [ ] 火狐浏览器
    - [ ] Chromium
  - [ ] NetBSD 安全加固
  - [ ] DragonFlyBSD 基础知识
    - [ ] 版本概况
    - [ ] 开发宗旨与项目目标
    - [ ] 注意事项
    - [ ] 跟踪新版本
    - [ ] pkgsrc
    - [ ] FreeBSD Ports
  - [ ] 换源与包管理器


## PDF 文档

> **PDF 文档导出流程**
>
> - 使用由 [safreya](https://github.com/safreya) 提供的脚本：
>   
>> 　　<https://github.com/FreeBSD-Ask/gitbook-pdf-export> 用于导出本书的 PDF 文档。该脚本使用 Python 3 编写，仅在 Windows 10、FreeBSD 14 上测试过。
>> 
>> 具体使用方法见该项目的 README.

## 概述

FreeBSD 从入门到跑路诞生于 2021 年 12 月 19 日。

本书定位：编写一本 FreeBSD 版本的《鸟哥的 Linux 私房菜：基础学习篇》&《鸟哥的 Linux 私房菜：服务器架设篇》。

**编辑指南概要**：我们欢迎所有支持 FreeBSD 的人进行编写，并会将其列入贡献者名单。

## 资源

QQ 群：787969044（须答题验证）

微信公众号: rpicn2025 （扫码关注）

![](./.gitbook/assets/qr.png)

Telegram 群组：[https://t.me/oh_my_BSD](https://t.me/oh_my_BSD)

Skype: [https://join.skype.com/xktkQtXZopfv](https://join.skype.com/xktkQtXZopfv)

FreeBSD 需要兼容层才能运行 QQ；Telegram 可原生运行；Skype 可使用 pidgin+ 插件 [net-im/pidgin-skypeweb](https://forums.freebsd.org/threads/skype.66115/)

HandBook 翻译：[https://handbook.bsdcn.org](https://handbook.bsdcn.org/)

FreeBSD Port 开发者手册翻译：[https://porters-handbook.bsdcn.org](https://porters-handbook.bsdcn.org/)

FreeBSD 入门书籍：[https://book.bsdcn.org](https://book.bsdcn.org/)

FreeBSD 中文 man 手册：[https://man.bsdcn.org](https://man.bsdcn.org/)

## 内容提要

《FreeBSD 从入门到跑路》 由 FreeBSD 中文社区发起。我们尝试从 0 开始，和所有人一同徜徉 FreeBSD 世界。

## 捐赠

![](.gitbook/assets/proud_donor.png)

[点此捐赠 FreeBSD 基金会](https://freebsdfoundation.org/donate)

有多的钱请捐给 FreeBSD 基金会吧。

