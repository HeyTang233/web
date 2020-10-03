---
---

# Debian镜像使用帮助

## 收录架构

  + 作为官方源之一，与 Debian 上游保持相同

## 收录版本

  + 与 Debian 上游保持相同

## 使用说明

操作前请做好相应备份 

一般情况下，更改 /etc/apt/sources.list 文件中 Debian 默认的源地址 [http://httpredir.debian.org](http://httpredir.debian.org/ "http://httpredir.debian.org") 为 [http://mirrors.ustc.edu.cn](http://mirrors.ustc.edu.cn/ "http://mirrors.ustc.edu.cn") 即可。 

Debian 的默认源地址可能依情况而不同，请注意更改 httpredir.debian.org 为合适的地址。 

可以使用如下命令： 

    
    
    sudo sed -i 's/httpredir.debian.org/mirrors.ustc.edu.cn/g' /etc/apt/sources.list

也可以直接编辑，以 Jessie 为例，编辑 /etc/apt/sources.list 文件，在文件最前面添加以下条目 

[sources.list](/wiki/_export/code/mirrors/help/sources435f.list?codeblock=0 "下载片段")

    
    
    
      deb http://mirrors.ustc.edu.cn/debian stable main contrib non-free
      deb-src http://mirrors.ustc.edu.cn/debian stable main contrib non-free
      deb http://mirrors.ustc.edu.cn/debian stable-proposed-updates main contrib non-free
      deb-src http://mirrors.ustc.edu.cn/debian stable-proposed-updates main contrib non-free

如果您使用的是 jessie 以外的版本，或者希望选择 IPv4/IPv6、HTTP/FTP，请使用我们的 **[配置生成器](https://mirrors.ustc.edu.cn/repogen/ "https://mirrors.ustc.edu.cn/repogen/")**

## 相关链接

  + 官方主页: <http://www.debian.org/>   

  + 邮件列表: <http://www.debian.org/support#mail_lists>   

  + Wiki: <http://wiki.debian.org/>   

  + 文档: <http://www.debian.org/doc/>   

  + 镜像列表: <http://www.debian.org/mirror/list>   
