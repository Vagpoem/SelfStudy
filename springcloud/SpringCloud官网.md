#### 官网 ####

**1.概述**

提供了一个快速的工具，快速构建分布式系统中的一些常见模式（例如，配置管理，服务发现，断路器，智能路由，微代理，控制总线，一次性令牌，全局锁，领导选举，分布式会话，群集状态），快速实现服务和应用程序，可以在任何分布式环境中正常工作。

**2.入门**

分为两种：

直接访问start.spring.io生成项目。

将springcloud添加到现有的springboot项目中，根据版本对应的关系选择相应的版本。在pom文件中添加以下信息

~~~xml
<properties>
    <spring.cloud-version>Hoxton.SR8</spring.cloud-version>
</properties>
<dependencyManagement>
    <dependencies>
        <dependency>
            <groupId>org.springframework.cloud</groupId>
            <artifactId>spring-cloud-dependencies</artifactId>
            <version>${spring.cloud-version}</version>
            <type>pom</type>
            <scope>import</scope>
        </dependency>
    </dependencies>
</dependencyManagement>
~~~



在idea中可直接在创建项目的时候添加相应的依赖。

**3.配置**

首先需要添加spring-cloud-config-server的依赖，同时配置主类注解@EnableConfigServer

~~~properties
spring.cloud.config.uri=http://localhost:8888
spring.config.name=configserver
spring.cloud.config.server.git.uri=file:... # 可以是本地的url，它是git存储库的位置
spring.cloud.config.server.bootstrap=true
~~~

**4.Netflix**

Spring Cloud Netflix的功能：（Spring Environment？）

服务发现：1.注册 2.创建并嵌入

断路器：1.注释驱动 2.Java配置嵌入

声明式REST客户端：

客户端负载均衡器：

外部配置：

路由器和过滤器：

需要添加spring-cloud-starter-netflix-eureka-server依赖并添加注解@EnableEurekaServer

**5.Bus**

将轻量级消息代理程序链接到分布式系统的节点。

