---
---

# Arch Linux 镜像使用帮助

## 收录架构

i686   
x86_64 

## 收录版本

ALL 

## 使用说明

编辑/etc/pacman.d/mirrorlist，先注释掉里面的所有行，然后在文件的最顶端添加 

[mirrorlist](/wiki/_export/code/mirrors/help/mirrorlist435f?codeblock=0 "下载片段")

    
    
    
    Server = http://mirrors.ustc.edu.cn/archlinux/$repo/os/$arch

## 相关链接

官方主页: <http://www.archlinux.org/>   
邮件列表: <http://www.archlinux.org/mailman/listinfo/>   
论坛: <http://bbs.archlinux.org/>   
Wiki: <http://wiki.archlinux.org/>   
