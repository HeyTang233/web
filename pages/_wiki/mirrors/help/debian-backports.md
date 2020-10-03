---
---

## Debian Backports镜像使用帮助

**注意：新版本 Debian Backports 已并入主源，单独的 `debian-backports` 目录只为兼容性保留。如需了解如何使用 `debian-backports` ，请参阅[官方文档](http://backports.debian.org/Instructions "http://backports.debian.org/Instructions")。**

* * *

### 收录架构

  + i386

  + amd64

  + source 

### 收录版本

stable-backports 

### 使用说明

以Squeeze为例, 编辑/etc/apt/sources.list文件, 在文件最前面添加以下条目(操作前请做好相应备份) 

    
    
    deb http://mirrors.ustc.edu.cn/debian-backports/ squeeze-backports main contrib non-free
    deb-src http://mirrors.ustc.edu.cn/debian-backports/ squeeze-backports main contrib non-free

### 相关链接

  + 官方主页: <http://backports.debian.org/>

  + 邮件列表: <http://backports.debian.org/Mailinglists/>

  + 镜像列表: <http://backports.debian.org/Mirrors/>
