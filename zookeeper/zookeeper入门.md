# 概述
zookeeper是一个开源的分布式的，为分布式应用提供协调服务的Apache项目。

# zookeeper工作机制

zookeeper从设计模式角度来理解：是一个基于观察者模式设计的分布式服务管理框架。它负责存储和管理集群关心的数据，然后接受观察者的注册，一旦这些数据的状态发生改变，zk就负责通知注册的观察者。

zookeeper = 文件系统+通知机制

# zookeeper特点
1. 一个leader，多个follower
2. 集群中只要有半数以上存活，zk就能正常服务。
3. 全局一致性，每个server保存一份相同的数据副本，client无论连接到哪个server，数据都是一致的。
4. 更新请求顺序执行，来自同一个client的更新请求按其发送顺序依次执行。
5. 数据更新的原子性，一次数据更新要么成功，要么失败。
6. 实时性，在一定时间范围内，client能读到最新数据。

# zk的数据结构
zookeeper数据模型的结构与Unix文件系统很类似，整体上可以看做一个文件树，每个节点成为znode,每一个znode默认都能够存储1MB的数据，每个znode都可以通过其路径唯一标识。

# zk的应用场景
1. 统一命名服务
2. 统一配置管理
3. 统一集群管理
4. 服务器节点上下线，软负载均衡

# zk安装
1. 安装jdk
2. tar -zxvf 
3. 修改配置   conf/zoo.cfg:
mv zoo_sample.cfg zoo.cfg

tickTime=2000  心跳的间隔时间
dataDir=/var/lib/zookeeper  存储 内存中的数据库快照
clientPort=2181 客户端连接需要的端口

# 启动
bin/zkServer.sh start
查看状态 bin/zkServer.sh status
退出服务  bin/zkServer.sh stop
# 连接zk
bin/zkCli.sh -server 127.0.0.1:2181