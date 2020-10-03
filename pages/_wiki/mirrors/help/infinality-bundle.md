---
---

# infinality bundle 镜像使用帮助

## 使用方法

请在 /etc/pacman.conf 里根据需要添加： 

    
    
    [infinality-bundle]
    Server = http://mirrors.ustc.edu.cn/infinality-bundle/$arch
    
    
    [infinality-bundle-multilib]
    Server = http://mirrors.ustc.edu.cn/infinality-bundle/multilib/$arch
    
    
    [infinality-bundle-fonts]
    Server = http://mirrors.ustc.edu.cn/infinality-bundle/fonts

如果在更新过程中遇到了签名错误, 您可以选择设置 SigLevel = Optional TrustAll , 或者通过执行以下命令导入公钥来解决 

    
    
    # pacman-key -r 962DDE58
    # pacman-key --lsign-key 962DDE58
    # pacman -Syy

## 相关链接

官方主页: <http://bohoomil.com/>

ArchWiki: <https://wiki.archlinux.org/index.php/Infinality>
