---
---

## Debian Security镜像使用帮助

### 收录架构

  + i386

  + amd64

  + source

### 收录版本

  + stable

  + testing

### 使用说明

操作前请做好相应备份 

一般情况下，更改 /etc/apt/sources.list 文件中 Debian Security 默认的源地址 <http://security.debian.org/> 为 <https://mirrors.ustc.edu.cn/debian-security> 即可。 

可以使用如下命令： 

    
    
    sudo sed -i 's/security.debian.org/mirrors.ustc.edu.cn\/debian-security/g' /etc/apt/sources.list

以 Jessie 为例, 编辑/etc/apt/sources.list文件, 在文件最前面添加以下条目(操作前请做好相应备份) 

[sources.list](/wiki/_export/code/mirrors/help/sources435f-2.list?codeblock=0 "下载片段")

    
    
    
    deb http://mirrors.ustc.edu.cn/debian-security/ jessie/updates main non-free contrib
    deb-src http://mirrors.ustc.edu.cn/debian-security/ jessie/updates main non-free contrib

### 相关链接

  + 官方主页: <http://www.debian.org/>

  + 邮件列表: <http://www.debian.org/support#mail_lists>

  + Wiki: <http://wiki.debian.org/>

  + 文档: <http://www.debian.org/doc/>

  + 镜像列表: <http://www.debian.org/mirror/list>
