---
---

# NPM镜像使用帮助

中科大镜像站的 npm 镜像是 <https://registry.npmjs.org/> 的反代。 

## 使用说明

编辑 `~/.npmrc` ，添加 

    
    
    registry=http://npmreg.mirrors.ustc.edu.cn/

若不想将本源设置为默认源，只想使用本源安装某个软件包，可在安装包时采用以下用法： 

    
    
    npm --registry http://npmreg.mirrors.ustc.edu.cn install <packagename>

中科大 npm 镜像支持 https 安全连接，如果您的网络运营商部署了缓存设备，或您对所处的网络环境不信任，请使用 `https` 替换上述 URL 中的 `http` 。 

## 注意事项

不支持 publish，若出现错误，请将 `~/.npmrc` 中的用户名密码部分注释掉，并删除缓存 ( `rm -rf ~/.npm` ) 重试。 

## 相关链接

官方主页: <https://www.npmjs.org/>
  *[URL]: Uniform Resource Locator
