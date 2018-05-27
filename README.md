# RESTful-web-service
RESTful web服务： Messages. 实现客户端与服务端之间的消息沟通，客户端发送消息到服务端，服务端进行响应答复 。
开始日期：2018年3月26日
成员：软件架构第六组
主题：通过HTTP的基础请求和响应服务来实现客户端与服务端之间的消息沟通。请求将采用GET或POST方法，回复将使用response code完成。

2018年4月6日
完成情况：使用websocket连接tomcat本地服务器，浏览器通过JavaScript向服务端发出建立WebSocket连接的请求，连接建立后，
客户端和服务端通过TCP连接传输数据。

2018年4月22日： 实现前后端分离
实现过程： 1.页面端通过API接口以GET、POST等HTTP标准方法进行请求、响应，并将结果以JSON数据的形式返回。
          2.使用vue.js进行数据请求和渲染, 为前端页面提供了相应的操作API接口。
          3.通过前后端分离，具有数据交互的页面当做SPA开发；后端只需为前端提供API接口。
          
2018年5月6日  用zookeeper实现的RPC框架
另外使用了Netty： 由JBOSS提供的一个java开源框架。Netty提供异步的、事件驱动的网络应用程序框架和工具，用以快速开发高性能、高可靠性的网络服务器和客户端程序。Netty封装了Socket处理。
服务发布：服务端使用Zookeeper注册服务地址，客户端从Zookeeper获取可用的服务地址。
通信：使用Netty作为通信框架。
动态代理：客户端使用代理模式透明化服务调用。
消息编解码：使用Protostuff序列化和反序列化消息。
服务端异步多线程处理RPC请求，客户端使用长连接（在多次调用共享连接），服务异步调用的支持，回调函数callback的支持

Reference:
http://www.cnblogs.com/luxiaoxun/p/5272384.html 一个轻量级分布式RPC框架--NettyRpc


2018年5月27日： Docker
docker 在下载image的时候,会在/var/lib/docker目录下创建相关的image 目录. 而运行的container则会放在/var/lib/docker/containers中.
docker中的image,是存储在docker仓库.
使用docker run的时候, 如果images里面没有存在指定的image时, docker会主动去docker hub里面找,然后下载,并且自动运行.
在拉取的时候,想知道这个image是否是真正存在的话,就可以使用.docker 提供的搜索指令.
在docker中,可以使用自带的search命令,搜索所有含有指定term的image. 相当于js中的search 方法.
使用了Dockerfile，是为了迅速的构建image。
