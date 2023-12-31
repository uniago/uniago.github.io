---
title: linux系统目录结构
date: 2023-11-10 04:33:34 +0800
categories: ['Tech','Linux']
tags: ['Linux']
---



## 系统启动必须

| 目录   | 说明                                                                                                                                                                                          |
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| boot | 存放的启动Linux时使用的内核文件，包括连接文件以及镜像文件                                                                                                                                                             |
| etc  | Etcetera（等等）的缩写，存放系统需要的配置文件，和子目录列表，更改目录下的文件可能会导致系统不能启动                                                                                                                                      |
| lib  | Library（库）的缩写，存放基本代码库（比如c++库），其作用类似于Windows里的DLL文件。<br />几乎所有应用程序都需要用到这些共享库                                                                                                                 |
| sys  | 这是linux2.6内核的一个很大的变化。<br />该目录下安装了2.6内核中新出现的一个文件系统 sysfs。<br />sysfs文件系统集成了下面3种文件系统的信息：<br />`针对进程信息的proc文件系统`<br />` 针对设备的devfs文件系统` <br />` 针对伪终端的devpts文件系统`<br />该文件系统是内核设备树的一个直观反映。<br />当一个内核对象被创建的时候，对应的文件和目录也在内核对象子系统中 |



## 指令集合

| 目录   | 说明                                                   |
|------|------------------------------------------------------|
| bin  | Binaries (二进制文件) 的缩写，存放着最常用的程序和指令                    |
| sbin | Superuser Binaries (超级用户的二进制文件) 的缩写，只有系统管理员能使用的程序和指令 |



# 外部文件管理

| 目录    | 说明                                                             |
|-------|----------------------------------------------------------------|
| dev   | Device(设备)的缩写, 存放的是Linux的外部设备。<br />注意：在Linux中访问设备和访问文件的方式是相同的 |
| media | 类windows的其他设备，例如U盘、光驱等等，识别后linux会把设备放到这个目录下                    |
| mnt   | 临时挂载别的文件系统的，我们可以将光驱挂载在/mnt/上，然后进入该目录就可以查看光驱里的内容了               |



## 临时文件

| 目录         | 说明                                                                                       |
|------------|------------------------------------------------------------------------------------------|
| run        | 是一个临时文件系统，存储系统启动以来的信息。<br />当系统重启时，这个目录下的文件应该被删掉或清除。<br />如果你的系统上有 /var/run 目录，应该让它指向run |
| lost+fonud | 一般情况下为空的，系统非法关机后，这里就存放一些文件                                                               |
| tmp        | temporary(临时) 的缩写，这个目录是用来存放一些临时文件的                                                       |



## 账户

| 目录       | 说明                                                                               |
|----------|----------------------------------------------------------------------------------|
| root     | 系统管理员的用户主目录                                                                      |
| home     | 用户的主目录，以用户的账号命名的                                                                 |
| usr      | unix shared resources(共享资源) 的缩写，用户的很多应用程序和文件都放在这个目录下，类似于windows下的program files目录 |
| usr/bin  | 系统用户使用的应用程序与指令                                                                   |
| usr/sbin | 超级用户使用的比较高级的管理程序和系统守护程序                                                          |
| usr/src  | 内核源代码默认的放置目录                                                                     |



# 运行过程中使用

| 目录   | 说明                                                                                                                                                                                  |
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| var  | variable(变量) 的缩写，存放经常修改的数据，比如程序运行的日志文件（/var/log 目录下）                                                                                                                                |
| proc | Processes(进程) 的缩写，管理内存空间！虚拟的目录，是系统内存的映射，可以直接访问这个目录来，获取系统信息。<br />这个目录的内容不在硬盘上而是在内存里，我们也可以直接修改里面的某些文件来做修改<br />例如,禁用ping指令: `echo 1 > /proc/sys/net/ipv4/icmp_echo_ignore_all` |



# 扩展使用

| 目录  | 说明                                      |
|-----|-----------------------------------------|
| opt | optional(可选) 的缩写，默认是空的，我们安装额外软件可以放在这个里面 |
| srv | 存放服务启动后需要提取的数据（不用服务器就是空）                |
