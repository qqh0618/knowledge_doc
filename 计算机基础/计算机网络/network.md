# 计算机网络
## 五层网络模型
1. 应用层 (要运输的东西):HTTP、DNS
2. 运输层(什么东西来运):TCP/UDP
3. 网络层(运到哪):IP
4. 链路层：帧的概念在此
5. 物理层：

## 应用层
1. HTTP：web缓存服务器、cookie、后端数据库；80端口号；TCP协议
2. SMTP协议;TCP协议
3. FTP:TCP
4. DNS(Domian Name System,DNS):一个由分层的**DNS服务器**实现的分布式数据库；一个使得主机能够查询分布式数据库的应用层协议。
   - 53端口
   - UDP协议
   - DNS通常有缓存，设置存储时间为2天。
   
   3.1 DNS记录报文
   
   资源记录

   (Name, Value, Type, TTL),TTL是该记录的生存时间，它决定了资源记录应当从缓存中删除的时间。Name和Value的值取决于Type。

   - Type = A：Name为主机名，Value为IP地址;标准映射
   - Type = ns:Name为域，Value是个知道如何获得域中主机IP地址的权威DNS服务器主机名
   - Type = CNAME：Value是别名为N啊么得主机对应的规范主机名。该记录能够向查询的主机提供一个主机名对应的规范主机名。
   - Type = MX, Value是个别名为Name的邮件服务器的规范名。
5. P2P文件分发：成功的有BitTorrent协议