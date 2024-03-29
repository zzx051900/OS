- 网课（黑马程序员）（共60节）：1、2、3、4、5、6、7、8、9、10、11、12

# 一.初始Linux

## （一）操作系统概述

- 个人桌面操作系统：Windows、macOS
- 服务器操作系统：Linux
- 计算机由**软件**和**硬件**组成
  - 硬件：计算机系统中由电子、机械和光电元件等组成的各种物理装置的总称
  - 软件：是用户和计算机硬件之间的接口和桥梁，用户通过软件与计算机进行交流，操作系统就是软件的一类

### 操作系统：

- 操作系统是计算机软件的一类，它主要负责：
  - 作为用户和计算机硬件之间的桥梁，调度和管理计算机硬件进行工作
- 操作系统可以：
  - 调度CPU进行工作
  - 调度内存进行工作
  - 调度硬盘进行数据存储
  - 调度网卡进行网络通讯
  - 调度音响发出声音
  - 调度打印机打印内容
- 常见操作系统：
  - PC端（个人电脑）：
    - Windows
    - Linux
    - macOS
  - 移动设备：
    - Android
    - IOS
    - HarmonyOS

## （二）初始Linux

- Linux创始人：林纳斯 托瓦兹
- 1991年创立

### Linux内核：

- Linux系统的组成如下：
  - Linux系统内核
  - 系统级应用程序
- 内核提供系统最核心的功能，如：调度CPU、调度内存、调度文件系统、调度网络通讯、调度IO等
- 系统级应用程序，可以理解为出厂自带程序，可供用户快速上手操作系统，如：
  - 文件管理器、任务管理器、图片查看、音乐播放等
- 比如播放音乐，无论用户使用自带的音乐播放器还是自行安装的第三方播放器，均是由播放器程序，调用内核提供的相关功能，由内核调度CPU解码、音响发声等
- 网址：https://www.kernel.org

### Linux发行版

- 内核是免费的、开源的，这就代表：
  - 任何人都可以获得并修改内核，并且自行集成系统级程序
  - 提供了内核+系统级程序的完整封装，称之为Linux发行版
- 常用知名的有：
  - Ubuntu、CentOS
- 不同的发行版：
  - 基础命令是相同的
  - 只有部分操作不同

## （三）虚拟机介绍

- 虚拟机：
  - 借助虚拟化技术，我们可以在系统中，通过软件：模拟计算机硬件，并给虚拟硬件安装真实的操作系统，即可以得到一台虚拟的电脑

## （四）VMware WorkStation安装

## （五）在VMware上安装Linux

- 本课程选用CentOS操作系统
- 网址：https://vault.centos.org/7.6.1810/isos/x86_64/
  - CentOS-7-x86_64-DVD-1810.iso

## （六）Mac系统Linux环境

## （七）远程连接Linux系统

- 学习目标：
  - 掌握操作系统的图形化、命令行两种操作模式
  - 理解为什么使用命令行操作Linux系统
  - 掌握使用 Finalshell 软件连接Linux系统

### 图形化、命令行

- 图形化：使用操作系统提供的图形化页面，以获得图形化反馈的形式去使用操作系统
- 命令行：使用操作系统提供的各类命令，以获得字符反馈的形式去使用操作系统

### 使用命令行学习Linux系统

- 尽管图形化是大多数人使用计算机的第一选择，但是在Linux操作系统上，这个选择被反转了。无论是企业开发还是个人开发，使用Linux系统，多数都是使用**命令行**
- 这是因为：
  - Linux从诞生至今，在图形化页面的优化上，并未重点发力。所以Linux操作系统的图形化页面：不好用、不稳定
  - 在开发中，使用命令行形式，效率更高，更加直观，并且资源占用低，程序运行更加稳定

### FinalShell

- 使用VMware可以得到Linux虚拟机，但是在Vmware中操作Linux的命令行页面不太方便：0/
  - 内容的复制、粘贴跨越VMware不方便
  - 文件的上传、下载跨越VMware不方便
  - 也就是和Linux系统的各类交互，跨越VMware不方便
- 我们可以通过第三方软件：FinalShell ，远程连接到Linux操作系统上，并且通过FinaShell去操作Linux系统，这样可以是各类操作系统变得十分方便
- 下载地址：
  - https://www.hostbuf.com/downloads/finalshell_install.exe
- 远程连接Linux操作系统：
  - 在VMware虚拟机中，桌面右键->Open Terminal->输入ifconfig->找到ens33：第二行IP地址
    - IP地址：192.168.17.132
    - （后续使用时IP地址可能会变，需要重新查找修改）
  - 在FinalShell中点击左上角文件夹图标，选第一个加号，SSH连接，名称随意设置，主机中输入IP地址，输入用户名和密码

## （八）拓展：WSL（Windows Subsystem for Linux）

- 掌握WSL获得Ubuntu系统环境
- 为什么要用WSL：
  - 轻量化，简单好用，省内存
  - 传统方式获取Linux系统是安装完整的虚拟机

- 什么是WSL：
  - 直接使用主机的物理硬件（无需通过虚拟机构建硬件），构建Linux操作系统，并不会影响Windows系统本身的运行

- WSL部署：
  - 右键开始按钮，应用和功能
  - 右上角，程序和功能
  - 左上角，启用或关闭Windows功能
  - 下翻，勾选适用于Linux的Windows子系统
  - 重启电脑
  - 微软应用商店下载Ubuntu和Windows terminal

## （九）拓展：虚拟机快照

- 我们可能损坏Linux操作系统，重装一个又很麻烦，通过快照可以把当前虚拟机 的状态保存下来，在以后可以恢复到虚拟机保存的状态
- VMware workstation Player没有快照功能，VMware workstation Pro才有快照功能
- VMware workstation Pro制作并还原快照：
  - 右键虚拟机，快照，快照管理器
  - 拍摄快照，取名，藐视，点击拍摄
  - 恢复快照，点击快照，转到

# 二.Linux基础命令

## （一）Linux的目录结构

- Linux的目录结构是一个树形结构，没有盘符，只有一个根目录/，所有文件都在根目录下
- Windows系统可以拥有多个盘符，如C盘、D盘
- Linux的路径描述方式：
  - 在Linux系统中，路径之间的层级关系，用 / 表示
    - 例：/user/local/hello.txt	（开头的 / 表示根目录）（后面的 / 表示层次关系）
  - 在Windows系统中，路径之间的层级关系，用 \ 表示
    - 例：D:\data\work\hello.txt

## （二）Linux命令入门

- 什么是命令和命令行：
  - 命令：Linux程序，一个命令就是一个Linux程序。命令没有图形化页面，可以在命令行提供字符化的反馈
  - 命令行：Linux终端，是一个命令提示符。以纯字符的形式操作系统，可以使用各种字符化命令对系统发出操作指令
- Linux命令的基础格式：
  - `command [-options] [parametor]`
    - connand：命令本身
    - -options：[可选，非必填]命令的一些**选项**，可以通过选项控制命令的行为细节
    - parametor：[可选，非必填]命令的**参数**，多数用于命令的指定目标
  - 示例：
    - `ls -l /home/itheima`
      - ls 就是命令本身，-l 是选项，/home/itmeima 是参数
      - 意思是：以列表的形式，显示/home/itmeima目录中的内容
    - `cp -r test1 test2`
      - cp 是命令本身 ，-r 是选项，test1 和 test2 是参数
        - 意思是：复制文件夹 test1 成为 test2 

## （三）目录切换相关命令

- ls 命令：
  - 作用：列出目录下的内容
  - 语法细节：`ls [-a -l -h] [Linux路径]`
    - -a -l -h 是可选选项
    - Linux路径是此命令可选的参数
  - 当不使用选项和参数时，直接使用 ls 命令本体，表示：以平铺的形式，列出工作目录下的内容

## （四）相对路径、绝对路径和特殊路径符

## （五）创建目录命令

## （六）文件操作命令

## （七）查找命令

## （八）grep、wc和管道符

## （九）echo和重定向符

## （十）vi编辑器

# 三.Linux权限管控

# 四.Linux实用操作

# 五.实战软件部署

# 六.脚本&自动化

# 七.项目实战

# 八.云平台技术



