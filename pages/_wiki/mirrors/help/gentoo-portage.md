---
---

# Gentoo-Portage镜像使用帮助

## 收录架构

## 收录版本

## 使用说明

旧的 SYNC 方式已不推荐使用，建议使用新的 repos.conf   
官网wiki：<https://wiki.gentoo.org/wiki//etc/portage/repos.conf>

### 单文件方式

新建或修改 /etc/portage/repos.conf ： 

[/etc/portage/repos.conf](/wiki/_export/code/mirrors/help/repos435f.conf?codeblock=0 "下载片段")

    
    
    
    [DEFAULT]
    main-repo = gentoo
     
    [gentoo]
    location = /usr/portage
    sync-type = rsync
    sync-uri = rsync://rsync.mirrors.ustc.edu.cn/gentoo-portage/
    auto-sync = yes

## 相关链接

官方主页: <http://www.gentoo.org/>   
邮件列表: <http://www.gentoo.org/main/en/lists.xml>   
论坛: <http://forums.gentoo.org/>   
文档: <http://www.gentoo.org/doc/en/>   
Wiki: <http://wiki.gentoo.org/>   
镜像列表: <http://www.gentoo.org/main/en/mirrors-rsync.xml>   
