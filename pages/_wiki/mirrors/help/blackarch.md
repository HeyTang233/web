---
---

# BlackArch 镜像源使用帮助

## 简介

BlackArch 是一款基于 ArchLinux 的为渗透测试及安全研究人员开发的发行版, 相当于 Arch 版的 BackTrack/Kali。 

仓库地址：blackarch.org/blackarch/ 

## 收录架构

i686   
x86_64   
ARMv6/7 

## 使用方法

在 /etc/pacman.conf 文件末尾添加两行： 
    
    
    [blackarch]
    SigLevel = Optional TrustAll
    Server = https://mirrors.ustc.edu.cn/blackarch/$repo/os/$arch

## 相关链接

BlackArch 主页： <http://blackarch.org>

收录的工具列表： <http://blackarch.org/tools.html>
