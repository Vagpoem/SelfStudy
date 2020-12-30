### SpringCloud ###

**1.基础概念**

集群、分布式、微服务、SOA

微服务：全能老师、分教研组、教研组内部所有人组成集群。

分布式：不同的角色负责不同的职责，大家共同协作完成任务。

集群：同一类角色分担所有到达的需求，共同处理任务。

微服务：将原先耦合在一起的一个大型的后台服务分解成很多个小型的微小服务。

Eureka：类似一张很大的注册表，存放了所有服务的信息，并且能够根据相应的信息调节负载情况。

Zuul：负责进行合法性的验证，防止非法访问。

Hystrix：及时处理一些突发的异常情况。

SpringCloud：就是综合上面所的部分形成的一个逻辑整体。

微服务通常基于HTTP的RESTful API。

SpringCloud是微服务框架，核心思想是分布式应用，专门为高并发、高负载、高可用而生。核心组件为：netflix、zuul、ribbon、feign和hystrix。

和SpringBoot的关系：SpringBoot专注于开发单个个体微服务，SpringCloud是关注全局的微服务协调、整理、治理的框架，他将SpringBoot开发的单体整合并管理起来，SpringCloud依赖于SpringBoot来开发微服务。

