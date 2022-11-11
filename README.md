# SanaeBot
易语言写的，从2011年开始写的屎山代码
缺少模块找不到的话可以问我要

全部功能文档&图解
https://www.yuque.com/km57bt/hlhnxg
太多了，所以放在可以折叠的语雀了

https://kook.top/VAKBfJ
里面也有获取onebot后端地址的程序

找不到后端地址可以联系我要
或者给我发邮件，applegm@me.com

后端太大了，所以放在云服务器上，想要本地部署也可以联系我

早苗可以缝合nonebot啦，缝合方法

首先按照nonebot教程部署nonebot2
https://v2.nonebot.dev/docs/start/installation
然后按照下面的文档安装nonebot2-gocq插件
https://github.com/mnixry/nonebot-plugin-gocqhttp

打开http://127.0.0.1:8080/go-cqhttp/#/
添加你的bot，并登录
点击修改设置-进程配置，打开config.yml，定位到尾部
将设置改为这个样子，请注意下方200xx，xx修改为1-50任意数字~以证明你不是机器人0w0
servers:

  - ws-reverse:
  
      universal: "{{{server_address}}}"
      
      reconnect-interval: 3000
      
      middlewares:
      
        <<: *default
        
        access-token: "{{{access_token}}}"
        
        servers:
        
  - ws-reverse:
  
      universal: "ws://sanae.youngmoe.com:200xx"
      
      reconnect-interval: 3000
      
      middlewares:
      
        <<: *default
        
        access-token: "{{{access_token}}}"


保存配置后，重启bot，看到启动时提示成功连接ws://sanae.youngmoe.com，代表你已经缝合成功了早苗
缝合成功后可以随意安装nonebot2插件结合早苗使用。
如何使用内置的澪和浅羽词库？请到kook频道获取后端ip获取器，然后替换到反向ws接口处使用，结合获取器（gocq实用工具）可以自动更换后端ip
交流群：674514951
