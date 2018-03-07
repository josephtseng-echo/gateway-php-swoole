# 网关 by php swoole develop
## 功能点
- tcp server 同时监听外网IP端口 及 内网IP端口
- 客户端client 连接外网IP端口通信 
- game server作为client 或 其他服务同样作为client 通过内网IP端口注册服务；并保持一条链路，通过server id(唯一)绑定链路fd  
- 客户端client 第一包必须登录验证包；通过验证后，将用户user id(唯一)绑定链路fd  
- 客户端client 通过包协议指定server id 跟 game server或其他server通信  
- gateway server负责转发客户端client 和 game server或其他server的通信包

...待补充