# gmall2020050801
电商项目每日代码更新

day01 
        第一次提交
            此次任务：搭建了单架构的user的服务。页面也可以查出结果

        第二次提交
            此次完成了：
            框架的基础部分的架构搭建（后面还有业务场景的架构）
            分别为gmall-parent/gmall-api/gmall-common-util/gmall-service-util/gmall-web-util
            各部分进行了引入依赖。
            并且能够运行，且浏览器能够读取和获取，完美！！！（20200508）

        第三次提交
            此次是试验git上存的准确性

        此处试验其他同时更改了代码
        
day02
        第一次提交
        
        第二次提交
            引入dubbbo+zookeeper框架
            那dubbo和zookeeper如何引入？
                dubbo其实是一组jar包，通过maven引入就可以。
                zookeeper是一个开源的服务软件，需要安装到linux中。
            dubbo的使用分为提供端和消费端。
            重点：使用起来非常方便只要记住两个注解@Reference和@Service《alibaba的依赖地址》
            加上application.properties的一段配置就可以了。
            
            然后使用服务器的ip地址对dubbo的监控中心进行查看，可以查看的服务的提供方和消费方的情况
            以及提及一下，就是dubbo的负载均衡策略有：随机/轮询和虽少并发及以上所有混用。四种方案。
            
            dubbo的基本概念
            服务的容器
            服务提供者（Provider）
            服务消费者（Consumer）
            注册中心（Registry）
            监控中心（Monitor）
            	dubbo调用关系说明
            	服务容器负责启动，加载，运行服务提供者。
            	服务提供者在启动时，向注册中心注册自己提供的服务。
            	服务消费者在启动时，向注册中心订阅自己所需的服务。
            	注册中心返回服务提供者地址列表给消费者，如果有变更，注册中心将基于长连接推送变更数据给消费者。
            	服务消费者，从提供者地址列表中，基于软负载均衡算法，选一台提供者进行调用，如果调用失败，再选另一台调用。
            	服务消费者和提供者，在内存中累计调用次数和调用时间，定时每分钟发送一次统计数据到监控中心。




