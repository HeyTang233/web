---
---

# Fedora镜像使用帮助

## 收录架构

  + i686

  + x86_64

## 收录版本

  + 所有仍在支持的版本

  + 最新测试版本

## 使用说明

将以下保存为 fedora-ustc.repo 

[fedora-ustc.repo](/wiki/_export/code/mirrors/help/fedora-ustc435f.repo?codeblock=0 "下载片段")

    
    
    
    [fedora] 
    name=Fedora $releasever - $basearch - ustc
    failovermethod=priority 
    baseurl=http://mirrors.ustc.edu.cn/fedora/releases/$releasever/Everything/$basearch/os/ 
    #mirrorlist=https://mirrors.fedoraproject.org/metalink?repo=fedora-$releasever&arch=$basearch 
    enabled=1 
    metadata_expire=7d 
    gpgcheck=1 
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-fedora-$basearch 
     
    [fedora-debuginfo] 
    name=Fedora $releasever - $basearch - Debug - ustc
    failovermethod=priority 
    baseurl=http://mirrors.ustc.edu.cn/fedora/releases/$releasever/Everything/$basearch/debug/ 
    #mirrorlist=https://mirrors.fedoraproject.org/metalink?repo=fedora-debug-$releasever&arch=$basearch 
    enabled=0 
    metadata_expire=7d 
    gpgcheck=1
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-fedora-$basearch 
     
    [fedora-source] 
    name=Fedora $releasever - Source - ustc
    failovermethod=priority 
    baseurl=http://mirrors.ustc.edu.cn/fedora/releases/$releasever/Everything/source/SRPMS/ 
    #mirrorlist=https://mirrors.fedoraproject.org/metalink?repo=fedora-source-$releasever&arch=$basearch 
    enabled=0 
    metadata_expire=7d 
    gpgcheck=1 
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-fedora-$basearch 

将以下保存为 fedora-updates-ustc.repo 

[fedora-updates-ustc.repo](/wiki/_export/code/mirrors/help/fedora-updates-ustccc37.repo?codeblock=1 "下载片段")

    
    
    
    [updates]
    name=Fedora $releasever - $basearch - Updates - ustc
    failovermethod=priority 
    baseurl=http://mirrors.ustc.edu.cn/fedora/updates/$releasever/$basearch/ 
    #mirrorlist=https://mirrors.fedoraproject.org/metalink?repo=updates-released-f$releasever&arch=$basearch 
    enabled=1 
    gpgcheck=1 
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-fedora-$basearch 
     
    [updates-debuginfo] 
    name=Fedora $releasever - $basearch - Updates - Debug -ustc
    failovermethod=priority 
    baseurl=http://mirrors.ustc.edu.cn/fedora/updates/$releasever/$basearch/debug/ 
    #mirrorlist=https://mirrors.fedoraproject.org/metalink?repo=updates-released-debug-f$releasever&arch=$basearch 
    enabled=0 
    gpgcheck=1 
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-fedora-$basearch 
     
    [updates-source] 
    name=Fedora $releasever - Updates Source - ustc
    failovermethod=priority 
    baseurl=http://mirrors.ustc.edu.cn/fedora/updates/$releasever/SRPMS/ 
    #mirrorlist=https://mirrors.fedoraproject.org/metalink?repo=updates-released-source-f$releasever&arch=$basearch 
    enabled=0 
    gpgcheck=1 
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-fedora-$basearch 

先备份/etc/yum.repos.d/fedora.repo和/etc/yum.repos.d/fedora-updates.repo 

将 fedora-ustc.repo和 fedora-updates-ustc.repo放入/etc/yum.repos.d/中 

运行： 

    
    
    sudo yum makecache 

更新缓存即可。 

## 相关链接

官方主页: <http://fedoraproject.org/>   
邮件列表: <http://fedoraproject.org/wiki/Communicate>   
论坛: <http://forums.fedoraforum.org/>   
文档: <http://docs.fedoraproject.org/>   
Wiki: <http://fedoraproject.org/wiki/>   
镜像列表: <http://mirrors.fedoraproject.org/publiclist>   
