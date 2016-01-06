---
layout: post
title: Mac OS X EI Capitan安装Scrapy的坑
---

前段可以参考 https://xdgcc.github.io/2015/10/04/%E5%8F%B2%E4%B8%8A%E6%9C%80%E5%AE%8C%E5%85%A8Mac%E5%AE%89%E8%A3%85Scrapy%E6%8C%87%E5%8D%97/。  
有一个坑，在删除老版本的`six`包的时候，可能文件被系统保护了，不允许操作。  
这是就需要先把这个SIP关掉，删掉低版本，装好高版本之后再打开。  


> 1. 重启 Mac，按住 Command+R 键直到 Apple logo 出现，进入 Recovery Mode
> 2. 点击 Utilities > Terminal
> 3. 在 Terminal 中输入 csrutil disable，之后回车
> 4. 重启 Mac

> 5. 删除包
```
    sudo rm -rf /System/Library/Frameworks/Python.framework/Versions/2.7/Extras/lib/python/six*
```
> 6. `sudo pip install six`

> 7. 重复1-4步，不过这次是用 csrutil enable 恢复SIP保护机制
> 8. 重启 Mac