# SanaeBot

专栏教程

https://www.bilibili.com/read/cv19705498

易语言写的，主要是2011~2016年epl时期的机器人代码

主要功能

传统的词库对话和教学学习系统（积攒了10年+的千万级语料库x3）

种菜、钓鱼、收集道具、寻找宝图、随机各种东西、各种亚文化功能

砍口垒式每小时群报时，早苗报时on

开播提醒，b站链接解析，定时计划任务（定时执行各种通知、指令）

各种禁言小游戏，轮盘禁言，禁言抽奖

gif图片模板生成功能，各种作者都不记得开发过了的稀奇古怪功能，

FF14任务查询、FF14道具查询、FF14板子查询

经过增强的Ai绘图，支持多线程生成，指定embeddings，指定不同模型


建议设置:

提及模式on

早苗提示off

脏话提醒off


方便零基础小白使用的nonebot2+早苗教程↓

https://www.bilibili.com/read/cv19705498

缺少模块找不到的话可以问我要

全部功能文档&图解

很多是不想失传，等着被人模仿到其他语言、框架的epl插件

https://www.yuque.com/km57bt/hlhnxg

功能都在语雀了，有耐心可以看看，有的挺好玩

https://kook.top/VAKBfJ

里面也有获取onebot后端地址的程序

找不到后端地址可以联系我要
或者给我发邮件，applegm@me.com

早苗的主要内容其实是数据库，放在云服务器上才能互通，想要本地部署可以自行用源码构建

早苗可以缝合nonebot、koishi，有对应的插件

nonebot-plugin-sanae和koishi-plugin-sanae

按照nonebot教程部署nonebot2

https://v2.nonebot.dev/docs/start/installation

按照下面的文档安装nonebot2-gocq插件

https://github.com/mnixry/nonebot-plugin-gocqhttp

打开http://127.0.0.1:8080/go-cqhttp/#/
添加你的bot，并登录
点击修改设置-进程配置，打开config.yml，定位到尾部
# 将设置改为这个样子，请注意下方200xx，xx修改为1-50任意数字

```
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
```
保存配置后，重启bot，看到启动时提示成功连接ws://sanae.youngmoe.com，代表你已经缝合成功了早苗
缝合成功后可以随意安装nonebot2插件结合早苗使用。
如何使用内置的澪和浅羽词库？请到kook频道获取后端ip获取器，然后替换到反向ws接口处使用，结合获取器（gocq实用工具）可以自动更换后端ip
交流群：674514951
