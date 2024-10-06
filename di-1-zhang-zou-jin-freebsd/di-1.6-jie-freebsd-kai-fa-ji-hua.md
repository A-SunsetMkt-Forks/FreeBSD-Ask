# 第 1.6 节 FreeBSD 开发计划

**翻译同步至 Mark a few things as completed**


> FreeBSD 的生命周期为每个大版本 4 年，小版本是发布新的小版本版后 +3 个月。
>
>
> FreeBSD 15 开发计划 [FreeBSD 15.0 Planning](https://github.com/bsdjhb/devsummit/blob/main/15.0/planning.md)


## FreeBSD 15.0 计划

### ✔️ 已完成

已提交到源代码存储库的项目。

| 项目                      | 负责人      | 已提交 / 审查 / 补丁                                                                                                                                                                               |
| ------------------------- | ----------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| arm64 分支目标识别（BTI）        | andrew      | [d09a64e15d8f](https://cgit.freebsd.org/src/commit/?id=d09a64e15d8fad6588b9aad62979f20afa8441df)                                                                                                   |
| arm64 bhyve               | andrew      | [47e073941f4e](https://cgit.freebsd.org/src/commit/?id=47e073941f4e7ca6e9bde3fa65abbfcfed6bfa2b)                                                                                                   |
| 在 bhyve 中的单步 AMD CPU | jhb Bojan   | [e3b4fe645e50](https://cgit.freebsd.org/src/commit/?id=e3b4fe645e50bfd06becb74e52ea958315024d5f)、 [ca96a942cafb](https://cgit.freebsd.org/src/commit/?id=ca96a942cafb58476e10e887240e594e7923a6e8) |
| 借助 CTF 美化 DDB 的输出| markj Bojan | [c21bc6f3c242](https://cgit.freebsd.org/src/commit/?id=c21bc6f3c2425de74141bfee07b609bf65b5a6b3)                                                                                                   |
| 跨架构的 kldxref              | jhb         | [0299afdff145](https://cgit.freebsd.org/src/commit/?id=0299afdff145e5d861797fe9c2de8b090c456fba)                                                                                                   |
| 在 install(1) 中实现 copy_file_range(2) | mmatuska    | [5a50d52f112a](https://cgit.freebsd.org/src/commit/?id=5a50d52f112a86ebd0696da6564c7c7befa27f5d)                                                                                                   |
| NVMe-oF/TCP               | jhb         | [a8089ea5aee5](https://cgit.freebsd.org/src/commit/?id=a8089ea5aee578e08acab2438e82fc9a9ae50ed8)                                                                                                          |
|基于单文件的 nullfs        | dfr         | [521fbb722c3](https://cgit.freebsd.org/src/commit/?id=521fbb722c33663cf00a83bca70ad7cb790687b3)（不支持套接字）                                                                                                                                                                        |
| 移植 9p 文件系统| dfr | [e97ad33a89a7](https://cgit.freebsd.org/src/commit/?id=e97ad33a89a78f55280b0485b3249ee9b907a718) |
|改进 NVMe Reset / Recovery | imp | [aa41354349c1](https://cgit.freebsd.org/src/commit/?id=aa41354349c16ea7220893010df78b47d67d0f74) |

### ✈️ 已实现

未来 2 年内 / 在下次发布之前已经存在且可以传递至上游的项目（也许需要努力使其达到可回馈上游的状态）

| 项目                              | 负责人         | 提交 / 审查 / 补丁                                                                                                                                                                                                                                                                                                         |
| --------------------------------- | -------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 在 mv(1) 中实现 copy_file_range()   | pjd            | [D45243](https://reviews.freebsd.org/D45243)                                                                                                                                                                                                                                                                               |
| 更好的 copy_file_range() 回滚机制/封装器 | pjd            | [D45243](https://reviews.freebsd.org/D45243)                                                                                                                                                                                                                                                                               |
| arm64 SVE                         | andrew         | [D43306](https://reviews.freebsd.org/D43306)                                                                                                                                                                                                                                                                               |
| amd64/arm64 急救内核              | markj / Klara  |                                                                                                                                                                                                                                                                                                                            |
| iovec 封装器                      | brooks         |                                                                                                                                                                                                                                                                                                                            |
| bhyve 虚拟机中的硬件监控功能        | jhb Bojan      |                                                                                                                                                                                                                                                                                                                            |
| 使用 DTrace 工具进行内联函数的跟踪     | markj Christos |                                                                                                                                                                                                                                                                                                                            |
| 谷歌编程之夏——squashfs         | chuck          |                                                                                                                                                                                                                                                                                                                            |
| 改进多核笔记本电脑上的 Powerd     | cperciva       | （与 gallatin@ 讨论）                                                                                                                                                                                                                                                                                                       |                                                                                                                                                                                                                                                                 
| CHERI 各式先决条件（ABI 位）      | brooks         |                                                                                                                                                                                                                                                                                                                            |
| 在 ZFS 中的分层速率限制           | pjd            | [16205](https://github.com/openzfs/zfs/pull/16205)                                                                                                                                                                                                                                                                         |                                                                                                                                                                                                                                      
| 简单的库 ABI 检查器               | brooks         | 原型在 [D44271](https://reviews.freebsd.org/D44271)                                                                                                                                                                                                                                                                                                                |
| 图形化安装程序                      | khorben        | [D44279](https://reviews.freebsd.org/D44279) [D44670](https://reviews.freebsd.org/D44670) [D44671](https://reviews.freebsd.org/D44671) [D44672](https://reviews.freebsd.org/D44672) [D44673](https://reviews.freebsd.org/D44673) [D44674](https://reviews.freebsd.org/D44674) [D45000](https://reviews.freebsd.org/D45000) |
| bhyve 直接使用 Linux 引导器           | 	robn           | （请参阅 [freebsd 虚拟化](https://lists.freebsd.org/archives/freebsd-virtualization/2024-May/002112.html)）                                                                                                                                                                                                                                                                                            |

### 🚧 正在进行

| 项目                                                              | 负责人        | 状态                                         |
| ----------------------------------------------------------------- | ------------- | -------------------------------------------- |
| AMD IOMMU 驱动程序                                                | kib           |                                              |
|重写 certctl                                                       | des           | [D42320](https://reviews.freebsd.org/D42320) |
| DRM 回归基本系统                                                      | manu          |完成 90%                                      |
| devd 事件磁盘错误额外信息                                       | imp           | 75%                                          |
| 对默认 TCP 堆栈模块化                                             | jtl           | 完成代码；需要 UX 支持、使用户更容易使用     |
| 真正有效的 UnionFS (overlayfs)                                 | olce          | 开始（在计划中）                           |
| 符合标准、实际的调度优先级                                        | olce          | 75%                                          |
| SO_SPLICE                                                         | Klara / markj | 刚开始                                       |
| 无头 bhyve                                                      | markj        | 进行中                                       |
| amd64 的 kboot 支持                                               | imp        | 2024 年夏末 80%                              |
| flua 和引导加载程序的更新至 Lua 5.4.7                              | imp        | 将在几周后发布，看起来“无聊”。     |
| 整合我谷歌编程之夏学生代码中的加载器命令行编辑功能 |imp     | 已有变基后的分支，需要帮助。               |
| riscv64 bhyve                                                     | br           |  [在虚拟机中启动 FreeBSD](https://wiki.freebsd.org/riscv/bhyve)                      |

### 💸 需要做的

未来两年内支持产品和服务所需的东西

| 项目                                                    | 负责人                        | 投入 / 审查 / 补丁 / 状态                                                               |
| ------------------------------------------------------- | ----------------------------- | --------------------------------------------------------------------------------------- |
| 新的 ELF 内核转储格式                                     | jhb markj                     |                                                                                         |
| 使 bsdinstall 支持 pkgbase                                 | emaste manu?                  |                                                                                         |
| 将 pkgbase 整合到发布和相关流程                         | 	bapt                       | 我们能否让每个包都有 Makefile                                                         |
| pkg 组                                                    | allanjude                       |                                                                                         |
| 为无工具链的 Poudriere 提供支持 jail                   | allanjude                     |                                                                                         |
| 外部工具链支持                                          | brooks                        |                                                                                         |
| 预提交 CI 源码、文档                                    | lwhsu imp bofh                | `make ci` 仍在开发，需要与 oth 集成                                                            |
| 改进 `make ci` 以方便提交者                      | imp、 bofh                     |                                                                                         |
| 改进 `make ci` 以对诸如登录 github 拉取请求等事项有益 | imp                           |                                                                                         |
| 预提交 CI ports                                         | lwhsu 将与 bapt 和 decke 审查 | bofh 似乎有一些 PoC                                                                     |
| 通用闪存存储（UFS）驱动程序                                    | loos                          | 需要用于一些嵌入式部署、但未来将更具通用性。即将登陆英特尔平台。同样支持 LinuxBoot。 |
| DTrace 的 `-C`（大写字母）参数再次生效                  | antranigv、markj              | PR 尚未提交、只需运行 `dtrace -c` 就可查看所含文件                                          |
| 完善了 bsd-user 支持以供发布流程使用                     | imp、 dfr、 cperciva            | 32 位系统在 64 位系统上的问题、对非常陈旧的 qemu-bsd-user-static 软件进行更新                |
| 优化 bsd-user binfmt 等以方便 jail 用户               | cperciva、 imp                 | Colin 希望每个 jail 都能设置这些事项                      |                                                             
| bsd bsd-user + poudriere 支持 RISCV                         | imp、 mhorne、 jrtc27           | 软件包构建完全损坏、但基本功能正常、需要修复以便我们可以再次使用 riscv 软件包           |
|使用 GitHub runner 拉取请求                             | 	imp                         | 针对 cirrus-ci 漏洞中的解决方案之一                                                           |
| 使用 GitHub Action 改善外部贡献者的体验                 | imp                           | 这里需要帮助                                                                       |
|  S0ix 低闲状态                                          | 	obiwac、 jhb                 |                                                                                         |
| 原生 inotify（2）                                       | tcberner                      | 许多软件都需要这个                                                                     |
| 15.0 应该使用哪个版本的 OpenSSL                         | gtetlow                       | 通过在现行环境中运行更新的版本以获取调试时间。                                                 |
| 不使用 OpenSSL FIPS                                   | gtetlow                       | 该模块没有经过验证、不要让人们上当                                                 |

### 🥺 想要 🙏

这些东西有当然最好、没有也行。

| 东西                                                                      | 拥有者                             | 提交 / 审核 / 补丁 / 状态                              |
| ------------------------------------------------------------------------- | ---------------------------------- | ------------------------------------------------------ |
| 清理 `make -s`                                                              | jhb                                | 清理警告信息并使其保持在控制之下 🔥                        |
| TPM 支持（GELI、ZFS）                                                     | allanjude tsoome                   | --                                                     |
| ZFS 加密启动支持                                                          | tsoome allanjude                   | 仅支持 UEFI                                            |
| 取代 smbfs（v2 及更高版本）                                               | emaste jhixson                     | --                                                     |
| virtio-fs                                                                 | ??? asomers                        | imp 表示有个补丁                                     |
| 在 Lua 中更新系统调用表生成（makesyscalls.lua 的库化）                    | imp                            |                                                        |
| 精简安装程序（使单个盘上的安装有更优的默认设置、一直按回车键就能完成）           | emaste brd                         |                                                        |
| 增补每个文件 file 以支持套接字/命名管道                                 | dfr                                |                                                        |
| 更多容器支持（OCI）                                                       | dfr                                | 需要志愿者。软件 Containerd 需要维护者。官方镜像/仓库  |
| 精简内核                                                                | imp                               | 进行中                                                 |
| 使引导加载程序支持 devmatch                                                 | imp manu	                        | PCI 和 USB                                             |
| 重写 config(8) （使用 lua ？）                                                | imp kevans                         |                                                        |
| 合并 devmatch 和 devd（库）                                             | imp                                | Meena 想帮助这个                                       |
| 调度程序和 VFS 的相关文档                                                   | mhorne、olce                       |                                                        |
| 在大小核心上进行调度（P、E）                                            | olce、mkarels                    | 我认为其他人感兴趣                                     |
| 完成内核文档（手册第 9 节）审核                                           | mhorne                             |                                                        |
| 简化过于复杂的解决方案                                                         | jhb imp                            |                                                        |
| vt(4) 更好的 i18n 支持（CJK 字体、unicode 字体显示（即表情符号）、输入法） | fanchung                            | 在 21 年谷歌编程之夏中有一个 [IME 概念验证](https://wiki.freebsd.org/SummerOfCode2021Projects/InputMethodInFreeBSDVirtualTerminal)                       |
| 以 root 运行 tarfs                                                              |imp                               |                                                        |
| overlayfs（用于 tarfs）                                                   | Klara / allanjude                   |                                                        |
| 内核中对 Rust 的支持                                                      | brooks                             |                                                        |
| 在用户空间支持 Rust                                                       | brooks                             |                                                        |
| 为 ZFS 提供 Netlink（zfsd/zed）                                           | allanjude                          |                                                        |
| 以 netlink 取代 devd 套接字                                                  | bapt                           | 具有内核部分                                           |
| 登录配置的 UCL 化                                                         | meena                              | allanjude 拥有初始补丁：[D25365](https://reviews.freebsd.org/D25365)                      |
| 为其余网络工具添加 libxo                                                  | meena                              | 如有问题请在提议的页面上 ping phil@                |
| 分层动态登录类                                                            | ngor、meena                        |                                                        |
| gve(4) 的 arm64 支持、GCE 的 arm64 实例需要                               | delphij、kibab（由 lwhsu 推动） |                                                        |
| 删除 MAC “label”的限制                                                   | 	allanjude des                         | 使用 OSD？建立在 bapt 的 mac_do 使用的每个 jail 机制上 |
| 用于 jail 的 PID 命名空间                                                | pjd dfr allanjude                  | 你想要哪些其他命名空间?                                |
| 将 dhcpcd 引入基本系统                                                    |                                    | 初始（日期）版本在这里：[D22012](https://reviews.freebsd.org/D22012)                         |
| 通过 netlink 访问 jail vnet                                               | dfr                                |                                                        |
| 在计算哈希值的同时能够在内存中操作文件。                                          | sjg (想参加)                        | 为 mac_veriexec                                        |
| 更新 flua、添加更多标准组件、更多“常见”组件及 FreeBSD 系统调用。      |                                    | 启动加载程序也使用 Lua、因此在这里需要小心些。       |
| priv(1)                                                                   | pjd                                | 降低进程权限的能力                                     |
| rctl                                                                      | DFR、PJD？                         | 当前 RCTL 对于资源限制 jail 的工作效果不佳            |

### 🗑️ 准备删除 🪓

我们可能希望废弃的项目。可能需要进一步讨论以达成共识。

| 项目                                                                                                          | 负责人          | 提交 / 审核 / 补丁                                                                        |
| ------------------------------------------------------------------------------------------------------------- | ---------------- | ----------------------------------------------------------------------------------------- |
| Firewire 🔥（火线）                                                                                                   | imp              | 宁愿晚一些而不是早一点（我们是否应该在更早的时候去除磁盘支持、因为有一个被 GIANT 锁定的 CAM 驱动程序）           |
| armv6                                                                                                         |	imp/manu       |                                                                                           |
| i386 内核                                                                                                     | imp             | 时间？                                                                                    |
| powerpc、powerpcsce 内核                                                                                      | imp              |                                                                                           |
| PS3 🎮                                                                                                        | imp               | 沒人使用了（我们需要移植 PS5！）                                                         |
| powerpc64、powerpc64le（整个 powerpc 架构）                                                                 |                  | <https://bugs.freebsd.org/271826> FreeBSD 在 PowerMac G5 上速度极慢……                     |
| SoC 评估审查                                                                                                 |imp/manu/mhorne	 |                                                                                           |
| ftpd                                                                                                          | allanjude        |                                                                                           |
| 移除 DES                                                                                              | des?             |                                                                                           |
| sendmail 📮                                                                                                   | bapt?           |                                                                                           |
|移除引导中的 Forth 语言 🔪                                                                                               | imp/stevek       |                                                                                           |
| 如果使用 EFI 启动安装程序但请求了 BIOS 安装，则发出警告                                                           |                  |                                                                                           |
| NIS 服务器组件                                                                                                | ~~des?~~         | 还在使用、请添加到 ports (chuck)                                                          |
| publicwkey(5)                                                                                                 | manu             | [D30683](https://reviews.freebsd.org/D30683) [D30682](https://reviews.freebsd.org/D30682) |
| targ(4) CAM 目标驱动程序                                                                                      | imp              |                                                                                           |
| fingerd                                                                                                       | ??               | Meena 想要做此事                                                                    |
| 3dfx(4) & `*_isa`                                                                                             | jhb              |                                                                                           |
| syscons(4)（至少不再推荐使用）                                                                         | emaste / manu    |                                                                                           |
| 以太网驱动程序（100mbps、冷门的 1/10 gbps）                                                               | brooks           |                                                                                           |
|  CAM 驱动程序（pms(4)、 hpt\*、 siis、 mvs 等）                                                              | imp              |                                                                                           |
| ACPI 安全定时器                                                                                               | cperciva           |     [00d061855deb](https://cgit.freebsd.org/src/commit/?id=00d061855deb93df5d709c8a794985ebb55012f8)                                                                                      |
| freebsd-update                                                                                              | cperciva            | 待 pkgbase 就绪                                                                      |
| 32 位平台（仅内核、仍保留 compat32）                                                                              | jhb              |                                                                                           |
| 移除 arm\*soft  (支持构建完整的软系统、这是在我移除了 libsoft hack 构建和 ld.so 支持之后剩下的全部内容) | imp              |                                                                                           |
| 支持交换内核堆栈                                                                                              | markj            |  [6aa98f78cc6e](https://cgit.freebsd.org/src/commit/?id=6aa98f78cc6e527b801cabddf6881ab5c9256934)                                                                       |
| 支持 SMP amd64 内核 !                                                                                          | markj         | 达成共识？ +1 +1                                                                              |

### 图例

| 符号 | 含义           |
| :----: | -------------- |
| ??   | 状态待定       |
| !!   | 需要新的负责人 |
