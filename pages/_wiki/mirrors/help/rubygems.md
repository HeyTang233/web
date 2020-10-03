---
---

# 替换gems默认源
    
    
    gem sources  #列出默认源
    gem sources --remove https://rubygems.org/  #移除默认源
    gem sources -a https://mirrors.ustc.edu.cn/rubygems/  #添加科大源

---
---

# 替换Rails默认源
    
    
    cd path/to/your/project
    #Linux only:
    sed -i "/^source/c source 'http://mirrors.ustc.edu.cn/rubygems/'" Gemfile 
    #OS X only:
    sed -ig "s/^source.*/source 'http:\\/\\/mirrors.ustc.edu.cn\\/rubygems\\/'/g" Gemfile  
