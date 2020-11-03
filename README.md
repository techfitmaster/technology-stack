
## Java基础

-  Java基础入门
- Java web开发
- 框架封装核心基础
	- 注解&反射API详解
	- 注解之框架封装实战
- Java开发基础
	- Java基础知识串讲
	- Java常用框架与工具回顾
	- Java开发能力必备

## 单点系统
### Springboot框架应用
- Springboot基础
	- Springboot基本介绍
	- Springboot快速入门
	- Springboot原理分析
	- Springboot配置
	- Springboot进行web开发
	- Restful的介绍及使用
	
- 数据库访问中间件
 	- Mybatis的回顾
 	- 使用Springboot整合rest和mybatis完成业务操作
 	- Springdata jpa的简介及快速入门
	- Springdata jpa的基本使用
	- Springboot 中的分页
- 数据库事务
	- 数据库事务的概念及实现原理
	- MySql事务隔离级别实战
	- Springboot中的事务处理

### 页面开发模版引擎
- 模版引擎
	- JSP模版引擎的回顾
	- FreeMarker的介绍及快速入门
	- FreeMarker的高级应用及和Springboot的整合
	- Thymeleaf的愈发详解及使用
	- Thymeleaf在Springboot中的应用	
- Servlet开发
	- Servlet的使用回顾
	- Struts2的使用回顾
	- SpringMVC的使用回顾


### Java核心基础
- Java程序运行原理分析
- 多线程核心
	- 线程状态
	- 线程中止
	- 内存屏障和CPU缓存
	- 线程通信
	- 线程封闭之ThreadLocal和栈封闭
	- 线程池应用及实现原理剖析

### JVM调优
- 性能测试
	- 功能与性能
	- 性能测试实操
- JVM性能优化实战
	- 类加载机制
	- 垃圾回收机制
	- JVM内置命令工具
	- JVM参数及调优
- Tomcat容器优化
	- TCP/UDP协议
	- BIO阻塞式网络编程
	- NIO非阻塞式网络编程
	- Tomcat网络处理线程模型
	- Tomcat参数优化


### 高并发优化
- 缓存优化
	- 了解内存缓存
	- 实现简单的内存缓存
	- 常见开源内存缓存工具介绍
	- caffeine实现原理-源码分析
	- 应对缓存同步、缓存穿透、缓存击穿、缓存雪崩
	- 内存框架设计与实现
	- 编写内存缓存框架中的核心模块
- 线程安全问题
	- 线程安全之可见性问题
	- 线程安全之原子锁操作
	- Java锁相关
- J.U.C并发编程包详解
	- Lock接口
	- AQS
	- 并发容器类-map-数组和链表
	- 并发容器类-map-hashMap初始化概述
	- 并发容器类-map-红黑树的基本概念
	- 并发容器类-map-hashMap的扩容机制
	- 并发容器类-map-concurretHashMap
	- 并发容器类-list_set_queque
	- 并发协同工具
	- FutureTask核心思想
	- forkjoin并发处理框架
- 异步优化
	- Websocket
	- Web容器的异步处理机制
- 单机限流
	- 单机限流算法及隔离策略
	- 低入侵限流框架设计与实现
	- 编写限流框架中的核心模块
	- OOM问题的解决与优化
	- CPU100%问题解决与优化


### Spring、Mybatis、Springboot原理
- Spring框架原理
	- Spring-IOC容器篇-自定义IOC容器
	- Spring-IOC容器篇-ApplicationContext
	- Spring-IOC容器篇-BeanDefinition
	- Spring-IOC容器篇-Bean生命周期
	- SpringAOP思想
	- SpringAOP源码流程
	- 事务的概念
	- 事务源码
	- Spring问题&核心流程分析
- Mybatis框架原理
	- Mybatis简介和优势
	- 手写Mybatis
	- Mybatis核心源码分析
	- 高级应用-分页插件
	- 高级应用-读写分离插件
	- 高级应用-缓存
	- 高级应用-自定义类型处理器

### Netty网络框架
- Netty框架源码学习
	- Netty线程模型
	- 责任链设计模式
	- 零拷贝机制
- Netty实践分享
	- 如何使用Netty支撑百万并发连接
	- Netty实战中的注意事项
- Spring Webflux
	- Reactor编程思想
	- Spring WebFlux详解
	- Spring WebFlux Web开发实战
	- WebFlux工作原理剖析

## 分布式系统

### Nginx
- 性能测试
	- 水平拓展与垂直拓展

- Nginx入门
	- Nginx负载均衡
	- 代理缓存机制
	- 通过Lua拓展Nginx
	- 高性能Nginx配置

- LVS负载均衡技术
	- LVS基础概念解析
	- 基于VIP的keepalived高可用架构讲解
	- 搭建LVS拒载均衡集群

- 云平台负载均衡技术
	- CDN实现应用的缓存和加速
	- DNS实现高可靠的负载均衡和访问提速
- Nginx实战技巧
	- Nginx配置Https
	- Lua拓展Ningx
	- Nginx缓存电商数据
	- 千万并发Nginx使用插件

- 负载均衡原理层
	- lvs+keepalived+nginx+tomcat实现高性能负载均衡集群
- 云平台负载均衡实战
	- DNS和CDN


### Redis
- Redis应用
	- Redis入门
	- Redis操作
	- 教你利用Redis支撑十万级并发
	- Spring与Redis集成方式及缓存注解原理
	- 直播系统后台接口中是如何使用Redis的
	- 基于Redis实现直播间聊天室后台支撑系统
	- 带你用Redis实现附近的帅哥美女查询功能
	- 发布订阅机制
	- Redis持久化机制
	- Redis内存管理
	- Redis主从复制
	- Redis哨兵高可用机制
	- Redis集群分片存储
	- Redis集群监控
	- 缓存失效导致雪崩的危害及应对方案
	- 缓存击穿的风险和应对方案

- Redis底层原理分析
  - Redis数据结构原理(1) -- string,hash,list
  - Redis数据结构原理(2) -- set,zset,stream
  - Redis数据结构实践之分布式锁的实现
  - Redis持久化
  - Redis主从模式原理
  - Redis Sentinel高可用组件
  - Redis cluster集群模式
  - 其他开源的redis 集群实现模式

- memcached
  - memcached协议支持
  - memcached工作原理以及优缺点
  - 缓存中间件实践之缓存和数据库一致性更新原则

### MySQL

- Mysql运行原理分析
  - Mysql运行结构
  - InnoDB整体架构
  - btree详解1之索引与磁盘操作的关系
  - 树型结构在索引中的应用
  - btree对二叉查找树的优化
  -  b+tree详解总结篇
  - ACID与InnoDB
  
 - SQL查询定位和优化
 	- mysql-workbench介绍
	- 慢SQL日志分析
	- 索引概述
	- 查询优化器与执行计划
	- 执行计划详解-selectType
	- 执行计划详解-accessType字段
	- 执行计划详解-extra字段 

- SQL查询技巧分析
	- Like会不会走索引
    - 索引列能不能为空
    - 函数计算会不会走索引
    - 类型不一致会不会走索引
    - Where条件顺序怎么写
    - 要不要用UNION替代OR
    - EXISTS VS IN
    - 非等于会不会走索引
    - 索引覆盖
    - 用子查询还是表关联
    - 表关联之大表小表
    - 分页的玩法
   
 - 数据库锁
    - MVCC多版本并发控制
    - 数据库-行级锁
    - 数据库锁-表级锁
    - 事务模型
  
 - 数据更新相关注意事项
    - 生产环境改表结构
    - insert导致的死锁
    - update导致的死锁
    - 分区表
   
- 数据库中间件设计
    - 数据库中间件核心理念篇
    - 数据库中间件设计要点
   
 - Mycat数据库集群中间件
    - mycat入门
    - 读写分离
    - 分库分表的场景
    - 数据库设计最佳实践
    
 - Sharding-jdbc数据库操作增强类库
    - sharding-jdbc概览
    - 基于客户端的读写分离
    - 分库分表
    - 事务与数据治理

### 安全基础知识
- 密码学基础
    - 常见的安全问题场景
    - 对称与非对称加密
    - Hash算法与碰撞
    - 签名、证书
 - 常见的安全问题
    - XSS、CSRF、DDOS
    - 请求重放与中间人（HTTPS）
- 会话
    - openId、oauth
    - sso
    - 实战：简易实现SSO
 - 搜索引擎ES
    - 搜索引擎核心理论思想
    - ES应用场景及核心概念
    - ES查询语法解析
    - ES高级查询
    - ES高性能集群
    - ELK实时日志分析平台

## 服务化改造
### 分布式系统拆分理论

- 微服务拆分理论
 	- 云课堂服务化拆分的背景
 	- 分布式系统架构演进之路
    - 服务化理论知识
    - 服务化的意义
    - 拆分原则介绍
- 微服务拆分步骤和方法
    - 识别业务领域及边界（第一部分）
    - 识别业务领域及边界（第二部分）
    - 领域划分和建模的方法
    - 领域划分的一些方法和经验
    - 企业级电商领域建模的真实案例解析
    - 企业级服务拆分的真实案例解析2

### 分布式系统拆分实践
- 分布式系统拆分实战  
    - 背景介绍
    - 课程说明
    - Dubbo为什么出现
    - Dubbo应用与整体结构
- JAVA RPC通信
    - RPC技术内幕
    - RPC框架整体设计与基础讲解
    - RPC框架如何与Spring集成
    - RPC底层网络框架设计
    - 网络协议设计与实现
    - Netty自定义协议开发
    - Invoker代理调用机制
    - 手写底层网络编码器
    - 手写服务注册机制
    - RPC注入动态网络代理
    - RPC长连接与多线程调用
    - 手写客户端负载均衡与服务发现
    - 手写RPC总结
    - Dubbo二次开发介绍
    - 项目演示：dubbo服务化项目实践
    - 技术分享（直播）-云课堂的dubbo实践-直播
- Maven模版工程搭建
    - 模版工程简介
    - 搭建自己的项目模板
    - 模版工程的维护策略
- 分布式系统解藕问题
    - 什么是耦合以及耦合带来的问题
    - 服务依赖解耦的方法
    - 依托于消息队列的架构设计和实践
    - 项目演示：服务依赖解耦实战

### 分布式消息中间件
- 分布式消息中间件 
    - 消息中间件概念和RabbitMQ介绍
    - Kafka技术架构和配置
    - RocketMQ介绍
    - 消息中间件之间的对比和使用的经验
 - 分布式消息中间件设计
    - amqp
    - mqtt
    - open message
    - kakfa协议
    - 持久化设计
    - 消息分发设计
    - 高可用设计
    - 可靠性设计
- Activemq
    - amq入门
    - amq支持的消息协议讲解
    - Activemq高可用集群方案
    - 持久化原理及事务机制

- Rabbitmq
    - rabbitmq入门及消息分发机制
    - rabbitmq集群和高可用方案
    - 持久化机制、内存/磁盘控制
    - 消息可靠性和插件化机制
- Kafka
    - kafka入门和使用场景
    - 消息持久化
    - 分片存储机制
    - Kafka Connect数据传输作业工具
    - Kafka Streams架构
    - 线程模型
    - 容错机制
    - Kafka优雅停机
    - 扩容
    - leader选举机制
- Rocketmq
    - rocketmq入门
    - rocketmq架构方案及角色详解
    - 有序消息
    - 订阅机制和定时消息
    - 批量消息和事务消息
    - RocketMQ中高性能最佳实践（包含消费者、生产者、JVM和Linux最佳配置）
   
 - MQ高并发应用
    - 超时关单、异步数据传输场景、超时关单、异步数据传输场景、定时任务调度场景（海量数据同步场景）

### Dobbo高阶实战

- Dubbo源码剖析 
    - Dubbo源码导读思路
    - Spring框架集成分析之ServiceBean对象
    - Spring框架集成创建ReferenceBean
    - Spring框架集成之Config对象命名
    - Spring框架集成之Dubbo组件生命周期
    - Spring框架集成之Dubbo引导器
    - Dubbo服务导出分析
    - 单协议单注册中心导出过程
    - 单注册中心单协议注册过程
    - 服务消费者之代理对象生成
    - Dubbo完整调用链路分析

- Dubbo特性  
    - Dubbo配置文件使用示例
    - Dubbo与SpringBoot集成
    - 启动时检查
    - 回声测试
    - 延迟连接
    - 集群特性
    - 多版本机制
    - 多实现类之服务分组

- Dubbo项目实践
    - dubbo实践之服务化思路分析
    - dubbo实践之系统设计与重构
    - dubbo实践之开发调试
    - dubbo架构实战之流控降级
    - dubbo架构实战之Hystrix集成
    - dubbo架构实战之Sentinel
    - dubbo架构实战之链路追踪
    - dubbo架构实战之配置中心
    - dubbo系统维护之路由调整
    - dubbo系统维护之优雅停机
    - dubbo更多实践+答疑直播（直播）

### Zookeeper

- Zookeepr核心功能和应用场景 
    - zk入门
    - zk核心概念（数据模型/会话机制/watch机制）
    - 详解分布式一致性协议: 2pc、3pc、PAXOS算法、Raft算法、zab
    - zk典型应用场景（用于实现配置中心/分布式锁）
    - zk集群

- 分布式锁
    - 分布式锁使用场景
    - 基于zk的分布式锁实现方案
    - 实战：分布式锁的技术选型及常见问题

- 分布式事务
    - 分布式事务来由
    - 分布式事务难点分析
    - 分布式事务分类
    - 强事务之Seata两阶段提交AT模式
    - 强事务之Seata-XA协议
    - 强事务之Seata-TCC方式
    - 弱事务之Seata-Saga模式
    - 弱事务之本地消息表
    - 分布式事务总结
    
- 分布式配置和链路追踪
    - 配置中心原理
    - 分布式监控中心

## 容器化服务
### Springcloud
- 微服务架构
    - 云课堂微服务背景介绍
    - 微服务的概念与优势介绍
    - 微服务与服务化的比较
    - 云课堂的一个微服务架构案例（1）
    - 云课堂的一个微服务架构案例（2）

- Springboot
    - springboot设计理念
    - 系统配置自动装载机制
    - starter快速集成机制详解
    - 使用actuator管理你的spring程序
    - 命令行工具springboot -cli快速构建项目

- Spring netlix组件
    - eureka服务注册与发现机制
    - ribbon客户端负载均衡机制
    - feign服务调用客户端
    - hystrix服务容错机制
    - zuul微服务网关组件

- Springcloud生态
    - config分布式配置中心
    - sleuth分布式系统链路追踪
    - gateway网关组件
    - consul服务注册与发现机制
    - stream消息驱动编程组件

- Sprincloud-alibaba
    - nacos服务注册中心
    - nacos配置中心
    - Sentinel服务保护机制
    - 分布式事务-seata

### Docker容器化技术
- Docker容器
    - docker介绍及使用
    - 容器网络互通和存储共享
    - 用docker改造xx服务实践

- Kubernetes编排
    - kubernetes核心概念及设计哲学
    - kubernetes的多副本控制器
    - kubernetes的负载均衡和服务发现
    - kubernetes 的网络(高级)
    - kubernetes 的数据卷(高级)
    - kubernetes的资源调度、故障容灾
    - 用kubernetes "一键"编排xx系统实战
- Kubernetes实战
    - 网易内部kubernetes容器实践分享

- Docker入门
    - 基础概念
    - 安装
    - 命令
    - 构建私有镜像
    - 运行Java程序
    - 搭建docker私有仓库

- Docker进阶
    - 数据挂载
    - Compose集成式应用组合及Service服务编排

- Docker实践
    - 容器监控
    - 日志监控
    - 资源管理
    - 快速扩容
### Git
- Git版本控制工具
    - git概述
    - git基础
    - git进阶
    - git协作开发

### Jenkins
- Jenkins
    - jenkins安装
    - jenkins使用
    - sonar使用


### 云原生DevOps
- 云原生CICD
    - 构建云原生体系与应用
    - CI/CD（上） 持续集成
    - CICD（下） 持续部署
- 监控
    - 使用prometheus监控，prometheus的整体介绍
    - 使用prometheus  operator快速部署prometheus
    - alert-mananger与报警

- 日志
    - 使用EFK技术栈采集检索日志，EFK技术栈整体介绍，filebeat、elasticsearch、kibana的部署
    - 容器日志采集的各种方式，如何使用Filebeat采集容器日志
    - Elasticsearch介绍，使用Kibana查询日志

### Service Mesh(微服务网络)

- Service Mesh
    - Service  Mesh背景介绍
    - Service  Mesh基础与价值
    - 控制面Istio介绍
    - 数据面Envoy介绍
    - 流量控制与服务治理功能介绍
    - 遥测（Trace、Metrics、Logging）介绍
    - 环境准备
    - 常用命令介绍
    - 基于轻舟Service  Mesh实现灰度发布、服务治理

## 职业化素养&项目管理

### 职业素养
- 职业素养
    - 从个人贡献者到团队贡献者的成长之路
    - 用画布设计你自己的职业发展路径
    - 用工具管理你的工作目标
    - 工作推进-互联网时代的时间管理
    - 沟通基础
    - 沟通风格
    - 工作中的情商密码
    - 问题分析与解决
    - 结构化表达上
    - 结构化表达中
    - 结构化表达下
    - 说服他人-搞定那个重要的他
    - 沟通中的冲突化解
    - 向上管理
    - 辅导他人的工具和技巧

### 项目管理
- 项目管理
    - 职业规划
    - 项目管理导学课
    - 项目管理框架概览课
    - 开好启动会
    - 明确项目目标
    - 识别项目干系人
    - 制定项目进度计划
    - 制定沟通计划
    - 管理项目风险
    - 项目的推进
    - 变更管理
    - 高效开会
    - 汇报项目进展
    - 项目复盘
    - 经验总结
 

