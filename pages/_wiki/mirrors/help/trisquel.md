---
---

# Trisquel镜像使用帮助

## 收录架构

ALL 

## 收录版本

Toutatis(6.0)   
Brigantia(5.5)   
Dagda(5.0)   
Slaine(4.5)   
Taranis(4.0)   
Awen(3.5)   
Dwyn(3.0)   
Robur(2.0) 

## 使用说明

Trisquel使用APT软件包管理系统，故其软件源使用方法与Ubuntu或Debian等很相似。 

以 Toutatis 为例, 编辑 /etc/apt/sources.list 文件 (需要使用 sudo), 在文件最前面添加以下条目(操作前请做好相应备份) 

    
    
    deb http://mirrors.ustc.edu.cn/trisquel/ toutatis main
    deb-src http://mirrors.ustc.edu.cn/trisquel/ toutatis main
    deb http://mirrors.ustc.edu.cn/trisquel/ toutatis-security main
    deb-src http://mirrors.ustc.edu.cn/trisquel/ toutatis-security main
    deb http://mirrors.ustc.edu.cn/trisquel/ toutatis-updates main
    deb-src http://mirrors.ustc.edu.cn/trisquel/ toutatis-updates main
    deb http://mirrors.ustc.edu.cn/trisquel/ toutatis-backports main
    deb-src http://mirrors.ustc.edu.cn/trisquel/ toutatis-backports main

## 相关链接

官方主页: <http://trisquel.info/en>
