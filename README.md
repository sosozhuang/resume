# 个人信息
### Shuo Zhuang


# 联系方式
- Programming: Java/Go
- Mobile：186****
- Email：sosozhuang@163.com
- GitHub: github.com/sosozhuang


# 工作经历

## 中信银行信用卡中心
### 技术架构  (2017.9 至今)
负责信用卡中心架构设计工作,负责微服务与容器化改造、云计算运维平台、云存储平台、中间件管控平台、运维管理平台等项目的建设。输出逻辑架构设计规范,应用系统同城双活建设方案,JVM 参数和Tomcat 参数优化方案等,指引开发团队,提升项目组协同能力。


## 惠普公司
### Systems Architect (2016.10 - 2017.8)
分布式一致性协议的设计与实现,负责 DevOps 项目的开发和设计,负责技术方案的研究实施,在实践中将方案落地,以 Kubernetes 和 Docker 为基础,提升开发项目的交付能力。


## 中国南方航空
### 架构师 (2015.10 - 2016.10)
负责电子商务移动端后台系统的需求分析和架构设计工作。编写项目设计方案,负责技术方案的研究实施,参与技术方案的评审,对存量代码进行优化和建立代码规范,解决核心代码性能问题。


## 中国工商银行
### 研发工程师 (2009.07 - 2015.10)
负责信用卡系统需求分析和编码设计工作。负责信用卡产品线研发;参与制定信用卡技术规范,负责主机代码服务重构,负责介质协议分离,非活动账户迁移,核心接口代码重构等项目的设计。


# 技能总结
- 5 年架构设计经验,11 年开发经验,独立带领开发团队的项目管理经验。
- 对多线程高并发编程,程序性能优化有丰富经验,熟悉 Java 和 Go 编程,Netty, Disruptor 等开源框架。
- 熟悉 Spring Cloud/Boot, Eureka, 配置中心, Hystrix,Zipkin,ELK 等微服务生态,多个项目实践经验。
- 熟悉 Kubernetes 和 Docker 等容器技术,多个项目涉及应用服务容器化改造。
- 熟悉 Kafka 消息队列技术,具备数十亿数据实时同步的项目经验。
- 熟悉 ElasticSearch 和 Redis,MySQL,Nginx 和 HaProxy 等技术。
- 熟悉 Ceph 分布式存储技术,了解云服务厂商对象存储方案。
- 熟悉 Prometheus 等监控告警技术,具备开发全链路监控体系的项目经验。
- 熟悉分布式一致性协议 Paxos 原理、实现和应用,具备编写生产环境可用的一致性框架能力。
- 熟悉 Spark, Spark streaming 和 Storm 等大数据编程技术。
- 熟悉 CI/CD 和 DevOps 流程, Git, Jenkins, Markdown 等工具。
- 阅读开源框架代码,阅读 paper。
  
  
# 项目经验
## 云计算运维平台 
#### 2020.04 至今
构建卡中心私有云平台,对基础设施如计算、网络和存储资源以及异构资源纳管;对平台服务如容器云、中间件和数据库,对平台运行服务如监控告警,计量计费,应用迁移和部署,多地多机房容灾等方面进行总体方案设计。规划上层应用系统接入方案,为应用系统和代运营系统提供高可用的
云平台。


## 云存储平台 
#### 2019.11 至今
#### Ceph, Kafka, ElasticSearch, Netty
基于 Ceph 建设卡中心分布式对象存储平台,将系统之间文件共享机制由本地写再传输方式升级为使用存储服务进行读写。支持多线程无锁并发写入同一对象文件,并进行内存复用,支持流式写入和上传,分摊传输流量,更加有效使用网络带宽。提供对象文件的发布订阅机制,消费方可使用元
数据作为条件表达式订阅文件,将定时轮询升级为实时推送,提升批处理效率。自研一套 Fluent API,支持同步、异步以及回调方式,提供可配置的负载均衡、限流、故障转移和重试等多种功能,使应用端接入方便并规范。同时跨机房的文件复制可按需定制,满足同城双活和异地灾备的数据备份要求。


## 中间件管控平台 
#### 2019.05 - 2020.05
#### Prometheus, Grafana, AlertManager, Kubernetes
对卡中心多个数据中心和机房的各类中间件,包括 NoSQL、MQ 和 LoadBalance 等,进行规范化管理,减轻开发和运行的维护压力。平台基于 Prometheus 和 Grafana 等开源组件,对中间件进行纳管监控、告警和处置,以及日志收集等。支持 Exporter 自动编排,标准化中间件服务,打造卡中心专有的中间件云服务。


## 新核心系统数据实时同步 
#### 2019.02 - 2019.05
#### MySQL, Canal, Kafka, Disruptor
新核心系统升级改造项目,将源数据从 MySQL Binlog 中实时同步到 Kafka 中,提供给外围系统进行实时计算、分析和消息通知等服务。经过分析火焰图和 profile,消除 false sharing、无锁设计和 CPU/IO线程隔离等深度程序性能优化,单节点 tps 达到 4 万+,生产环境集群 tps 高峰期可高达 180 万。满足了新核心系统上线时,数十亿级别的存量数据在短时间窗口内完成迁移,升级后增量数据在秒级完成同步的目标,同时满足数据严格时序、异常情况下无丢失的要求。


## 微服务架构升级改造 
#### 2017.09 - 2019.01
#### Spring Cloud/Boot, Kubernetes, Eureka, Hystrix, Zipkin, ELK
基于 Spring Cloud 生态作为微服务框架,Kubernetes 作为容器资源调度框架,包括服务注册和发现,负载均衡,配置中心,调用链追踪,日志收集,应用状态监控,熔断降级和限流等特性。


## CMDB 配置数据库 
#### 2018.08 - 2019.01
#### ElasticSearch
面向应用服务为中心构建卡中心 CMDB 配置信息库,为运维管理平台元数据的生产和消费能力提供支撑,为卡中心 CI/CD 流程、自动化体系和监控体系等平台提供统一的元数据管理服务。基于ElasticSearch 自研可动态配置的元数据模型,极大地降低数据模型不断变化带来的开发工作量。


## 批处理资源调度框架 
#### 2018.02 - 2018.07
#### Spring Cloud/Batch, Eureka, Ribbon, Quartz
调度框架支持在分布式环境下,将不同类型(CPU/MEM)的批处理任务分配到集群中的服务器资源执行。资源调度算法可根据任务类型,运行在制定的服务器上,达到集群资源的合理分配。在动态扩容、缩容或服务器宕机时,能够支持重新加载可用服务器资源列表。


## 分布式一致性协议框架
#### 2017.02 - 2017.08
#### Paxos, protobuf, LevelDB, RocksDB
基于 Multi-Paxos 一致性协议实现,支持响应时间优先的并发提交和吞吐量优先的批次提交,基于异步消息传递机制,支持 Leader 选举功能,动态变更集群节点, observer 模式快速接收快照数据,网络模式支持 TCP 和 UDP,存储模式支持纯内存和 mmap,支持 fsync 保证写入数据一致性,支持LevelDB 和 RocksDB 作为底层存储,支持历史数据的清理,使用 crc32 校验数据。


## 基于 Kubernetes 的 DevOps 方案
#### 2016.10 - 2017.08
#### Kubernetes/Docker, flannel, Etcd, MySQL
随着容器在生产环境扮演越来越重要的角色,而微服务成为大型软件系统的基础架构,如何整合开发、运维、测试和部署等流程成为项目组的迫切需求。该项目以 Kubernetes 作为构建 DevOps 的核心编排引擎,Docker 容器作为 DevOps 任务的运行基础环境,整合 CI/CD,实现便捷的自动化部署工作流。


## 服务治理与微服务改造
#### 2015.05 - 2016.10
#### Dubbox, Spring, Netty, Zipkin, MySQL
对电商平台系统进行微服务改造,基于 Dubbox 框架并将服务部署在 Docker 集群中运行,同时对其进行扩展升级,包括 Dubbox-sync,Dubbox-Netty4 和 Dubbox-brave-filter 等项目。使用CompletableFuture 支持异步非阻塞链式调用多个不同的服务,使用 Netty4 对传输层协议改造,添加了拦截接口支持记录客户端和服务端的消耗事件和依赖关系,支持拓扑图形化展示。


## 基于 Docker 的容器云方案
#### 2016.04 - 2016.10
#### Dubbox, Spring, Netty, Zipkin, MySQL
涵盖了应用容器化改造,持续集成构建,集群网络搭建,持久化存储,集群资源管理和任务调度,服务注册及发现,容器集群监控和健康检查,日志收集和分析,灰度发布等方面,支持开发、测试和生产环境的快速部署和横向扩展,是一套完整的解决方案。


## 流量控制和服务降级方案
#### 2016.03 - 2016.05
#### Nginx/lua, Redis
监控系统采集系统运行信息,触发相应的告警,实时调整流量控制系统的运行级别。在 Nginx 上使用 lua 对请求进行访问控制,对不同优先级的服务进行放行、限制或熔断。在高并发场景下,保证高优先级服务的可用性。包含监控和告警,限流规则管理,流量控制几个模块。


## 电商后台防爬虫系统
#### 2015.11 - 2016.10
#### Nginx/lua, Flume, Kafka,ElasticSearch/Kibana, Tomcat, Storm,Redis,MySQL
使用 Nginx+lua 对业务请求进行实时监控处理,非阻塞模式发送到消息采集系统;采集系统将消息复制分发,存储到 Kafka 和 ElasticSearch 中;Kafka 将数据导入到 storm 集群中进行流式分析,再根据配置规则进行分析,通过访问频率、IP 黑名单等防爬虫策略将异常请求数据登记;lua 的 access模块对请求报文进行拦截处理,监测到异常请求将拒绝服务或返回验证码。系统各个模块均可水平扩展或主备,保证了高并发下的高可用。


## 集群环境下会话共享方案
#### 2015.11 - 2016.01
#### Tomcat, Spring, Redis
在构建可水平扩展的分布式系统中,使用 Nginx 在前端拦截请求,转发给后端的 Tomcat 服务器时,共享用户会话数据;在主动停机或异常宕机后,能重新恢复会话。方案将 Tomcat 集群中的 session数据和状态进行集中存储到外部 Redis 服务器上,实现了自由控制 session id 如何在客户端和服务器之间进行交换,因此能容易地编写 Restful API,而不再依赖于 cookie。


## 移动电商后台监控系统
#### 2016.01 - 2016.02
#### Zabbix, Nginx, Redis, MySQL, Tomcat
对后台服务器的 CPU,负载,内存和磁盘 IO 进行监控及数据可视化展现,监控系统提供了对 Nginx、Tomcat、MySQL 和 Redis 的实时监控、记录和预警,对应用服务可用性的定时检测,触发异常事件时能发送邮件和短信进行告警。


## Java EE 平台构建 RESTFul 服务
#### 2015.03 - 2015.06
#### Java, Tomcat, RESTEasy
使用 RESTEasy 为自主研发的 Java EE 框架构建 RESTful 的 Web 服务,支持通过配置资源文件动态创建 REST 接口,并注入到 RESTEasy 框架中,
提高应用开发人员的开发效率和降低学习成本。实现 OAuth认证框架,在 REST 倡导的无状态模式下不使用 session,允许对受保护资源进行访问。


## 分布式缓存管理控制台
#### 2014.11 - 2015.01
#### LevelDB, Zookeeper, MyBatis, MySQL, JQuery, Tomcat
自研 KV 分布式缓存,使用 ssdb(LevelDB +Redis protocol)作为 NoSQL 数据库,为应用系统提供存储方案。一主双从实现高可用,zookeeper 作为分布式协调服务,通过一致性哈希保证数据均衡分布。该系统为分布式缓存提供自动化运维平台,包括用户管理,事件监控,运行监控,集群管理,机器管理和统计分析等模块。


## 源代码搜索分析
#### 2014.05 - 2014.07
#### Python, Django, MySQL, Sphinx
该工具为提高编写项目详细设计范围,编写代码效率,减少代码错误而开发,在工商银行使用 EGL开发系统中使用。使用 Python 解析源代码,生成调用关系链,web 框架使用 Django,后台数据库使用 MySQL,搜索引擎使用 Sphinx。支持正则表达式搜索,详细视图和多关键字交集搜索。


## 工商银行信用卡系统建设
#### 2009.07 - 2014.06
包括多币种卡、非活动账户数据迁移、个人综合授信系统、额度管理平台等项目的开发和设计工作。

