---
---

## Scientific Linux 镜像使用帮助

### 收录版本

6 

### 使用说明

下载sl-ustc.repo放入/etc/yum.repo.d/中 

[sl-ustc.repo](/wiki/_export/code/mirrors/help/sl-ustc435f.repo?codeblock=0 "下载片段")

    
    
    
    [sl]
    name=Scientific Linux $releasever - $basearch - ustc.edu.cn
    baseurl=http://mirrors.ustc.edu.cn/scientificlinux/$releasever/$basearch/os/
    #mirrorlist=http://ftp.scientificlinux.org/linux/scientific/mirrorlist/sl-base-6.txt
    enabled=1
    gpgcheck=1
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-sl file:///etc/pki/rpm-gpg/RPM-GPG-KEY-sl6 file:///etc/pki/rpm-gpg/RPM-GPG-KEY-cern
     
    [sl-security]
    name=Scientific Linux $releasever - $basearch - security updates - ustc.edu.cn
    baseurl=http://mirrors.ustc.edu.cn/scientificlinux/$releasever/$basearch/updates/security/
    #mirrorlist=http://ftp.scientificlinux.org/linux/scientific/mirrorlist/sl-security-6.txt
    enabled=1
    gpgcheck=1
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-sl file:///etc/pki/rpm-gpg/RPM-GPG-KEY-sl6 file:///etc/pki/rpm-gpg/RPM-GPG-KEY-cern
     
     
    [sl-source]
    name=Scientific Linux $releasever - Source - ustc.edu.cn
    baseurl=http://mirrors.ustc.edu.cn/scientificlinux/$releasever/SRPMS/
    enabled=0
    gpgcheck=1
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-sl file:///etc/pki/rpm-gpg/RPM-GPG-KEY-sl6 file:///etc/pki/rpm-gpg/RPM-GPG-KEY-cern

运行yum makecache 生成缓存 
