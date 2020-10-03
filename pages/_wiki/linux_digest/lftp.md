---
---

# lftp

[lftp](https://en.wikipedia.org/wiki/lftp "https://en.wikipedia.org/wiki/lftp")是一款基于命令行的文件传输程序。除了FTP外，她还支持FTPS, HTTP, HTTPS, HFTP, FISH和SFTP。它还有一个实用的特性，支持FXP，即在两台FTP服务器间传文件，绕过客户机。此外，她还有一个内建的BitTorrent客户端。 

## 常用命令

## 配置文件

lftp启动后会一次读取/etc/lftp.conf、~/.lftprc和~/.lftp/rc。 通常我们将常用的设置写入~/.lftprc或者~/.lftp/rc中。 下面是一份lftprc的样例： 

[.lftprc](/wiki/_export/code/linux_digest/435f.lftprc?codeblock=0 "下载片段")

    #在浏览GBK编码的ftp时，可以执行gbkserver命令迅速切换。
    alias gbkserver set ftp:charset gbk;set file:charset utf-8
    alias utfserver set ftp:charset UTF-8;set file:charset utf-8
     
    #使得ls的输出更友好、美观
    alias ls cls -lhSF
    set color:use-color true
     
    #本地文件名使用utf8存储
    set file:charset utf-8
     
    #对202.38.64.22站点的独立设置
    set ftp:passive-mode/202.38.64.22 no
    set ftp:charset/202.38.64.22 gbk

在被动模式下，lftp主动连接服务器进行数据传输。在主动模式下，服务器会主动连接lftp进行数据传输。 被动模式当您在防火墙后面时很有用。 

## 书签支持

将站点加入书签有两种简单常用的方法，一种是在命令行中执行bookmark命令： 

    bookmark add <name> [<location>]

改命令将会在~/.lftp/bookmarks文件中新增一行，内容类似如下： 

    movie	ftp://upload@202.38.64.22/

另一种方法就是直接编辑~/.lftp/bookmarks文件，例如我直接增加以下该行到文件中： 

    home    ftp://myname@home.ustc.edu.cn/public_html/

将来只需要在shell中执行： 

    lftp home

即可打开连接到我的ftp上了

![:-\)](../lib/images/smileys/icon_smile.gif)

## 奇巧淫技-使用lftp同步个人主页

科大的童鞋们都有一个300M的静态主页空间，很多人都会用这个空间来制作漂亮的个人主页，那你是怎么同步的呢？是不是每次都需要打开nautilus或者filezilla等工具一个个文件的复制呢？ 来看看用lftp的脚本同步吧。 

[.bash\_aliases](/wiki/_export/code/linux_digest/cc37.bash_aliases?codeblock=1 "下载片段")

    alias update-homepage='lftp -f ~/.bin/update-homepage.lftp'

[update-homepage.lftp](/wiki/_export/code/linux_digest/update-homepagec273.lftp?codeblock=2 "下载片段")

    connect home.ustc.edu.cn
    user myname
     
    mirror -R -e ~/public_html public_html --exclude book/ --exclude bak/

在这个lftp脚本中，首先连接服务器，然后使用mirror -R来将本地的~/public _html目录同步到服务器上的public_ html中，在我本地的目录中有bak目录，我不希望同步上去，就将它排除掉，另外book目录比较大，希望自己手动管理同步，所以也排除了。如果在服务器上有一个目录，本地没有，也可以将其排除，以免同步时被删除。 

以后本地文件修改之后，只需要执行 

    update-homepage

即可完成同步工作。也可将lftp -f ~/.bin/update-homepage.lftp这条命令写入[crontab](/wiki/linux/crontab "linux:crontab")，每天自动同步。 
