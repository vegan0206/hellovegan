# webChat
**功能介绍：** 这是一个基于nodejs+mongoDB+socket.io+vue实现的一款点对点聊天系统。由于开发需要，引进gulp和browser-sync，实时查看编写效果。由于没有做搜索联系人功能，系统默认配置了一个名为admin的用户，登陆的用户都会和admin成为彼此的好友。用于测试发送接受消息。

**已完成的功能：**
	
1. 登陆注册功能
2. 实时发送接收信息
3. 用mongoDB保存用户和消息记录

**未完成功能：**

1. 离线信息提醒
2. 未读信息提醒
3. 标记已读信息
4. 上传个人头像
5. 发送文件
6. 联系人分组
7. 联系人按照最后一次发送消息的时间进行排序
8. 界面可以再美一点
9. 。。。

#文件介绍
说明： 由于是用express生成器生成的项目结构，所以基本再原来的基础上没有做改过，可参照官网的项目结构和说明。这里只介绍新增的的文件结构。

**lib:**
库文件。包含mongoDB、socket的配置文件和util中自定义的一些方法。



-  mongo

	包含mongoDB的配置和用户模型、消息模型的配置


- websocket

	包含socket服务器基本配置和用户以socket协议连接时的一些事件处理函数。 

**public：** 分离src和build文件，并设置build目录为默认静态文件目录。

**uploads：** 上传文件的缓存目录

**view:** 由于前端采用vue实现，并没有用到vue里面的jade模板，里面的文件只做测试用。

**addDefaultUser.bat** 添加默认用户列表到数据库中的脚本文件，已配置admin用户，如需要可以在lib/mongo/user/defaultUserList.js 中配置。

**start.bat**  为了方便每次启动项目，默认配置脚本文件启动该。可以用gulp+browser-sync的方式和superisor的方式，注释相关的即可。


一些独白： 做一个这样的东西也是由于一时兴起，花了一些时间去了解相关知识，然后自己动手尝试了一下。 时间有限、精力有限、目前就先做到这个样子吧。等缓过这段时间，再去仔细的了解，做一个能直接用的在线聊天出来。 有很多事情都在改变，前方未必会有天堂，但地狱一定在身后。勿忘初心，共勉~
