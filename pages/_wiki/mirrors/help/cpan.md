---
---

## CPAN镜像使用帮助

### 使用说明

若你以前从未使用过CPAN，请在命令行下运行cpan 

    
    
    Would you like me to automatically choose some CPAN mirror sites for you? (This means connecting to the Internet) [yes] 

此处输入no 

    
    
    Would you like to pick from the CPAN mirror list? [yes] 

此处直接回车 

    
    
    You should select more than one (just in case the first isn't available).
    
    (1) Africa
    (2) Asia
    (3) Europe
    (4) North America 
    (5) Oceania
    (6) South America
    Select your continent (or several nearby continents) [] 

此处选择2 

    
    
    (1) China
    (2) India
    (3) Indonesia
    (4) Israel
    (5) Japan
    (6) Kazakhstan
    (7) Pakistan
    (8) Republic of Korea
    (9) Saudi Arabia
    (10) Singapore
    (11) Taiwan
    (12) Thailand
    (13) Turkey
    (14) Viet Nam
    Select your country (or several nearby countries) [] 

此处选择1 

    
    
    (1) ftp://ftp.cuhk.edu.hk/pub/packages/perl/CPAN/
    (2) ftp://mirror.communilink.net/CPAN/
    (3) ftp://mirrors.sohu.com/CPAN/
    (4) ftp://mirrors.ustc.edu.cn/CPAN/
    (5) ftp://mirrors.xmu.edu.cn/CPAN/
    (6) http://cpan.communilink.net/
    (7) http://ftp.cuhk.edu.hk/pub/packages/perl/CPAN/
    (8) http://mirror.qdu.edu.cn/CPAN/
    (9) http://mirrors.163.com/cpan/
    (10) http://mirrors.btte.net/CPAN/
    (11) http://mirrors.devlib.org/cpan/
    (12) http://mirrors.sohu.com/CPAN/
    (13) http://mirrors.ustc.edu.cn/CPAN/
    (14) http://mirrors.xmu.edu.cn/CPAN/
    Select as many URLs as you like (by number), put them on one line, 
    separated by blanks, hyphenated ranges allowed
     e.g. '1 4 5' or '7 1-4 8' []  

此处选择13 

其它问题视具体情况选择即可 

若你已经用过cpan了，将~/.cpan/CPAN/MyConfig.pm中的'urllist'的值改为 

    
    
    'urllist' => [q[http://mirrors.ustc.edu.cn/CPAN/]],

### 相关链接

  + 官方主页: <http://www.cpan.org/>

  + 镜像列表: <http://www.cpan.org/SITES.html>

  + FAQ: <http://www.cpan.org/misc/cpan-faq.html>

  *[FAQ]: Frequently Asked Questions
