# Docker_RocketMQ

## Win10开发环境下部署开发环境

    1.进入rocketmq_win文件夹
    2.执行命令部署 docker-compose up -d启动实例
    3.注意端口不要冲突，尤其是8080端口为控制台网站端口
    4.最重要一点，需要修改broker节点的 [broker.conf] 文件，如果修改了brokerIP1为宿主机IP则dashboard中显示无法连接到集群, 如果不修改,则通过程序无法连接到broker集群

        1>.将配置文件中新增配置 brokerIP1=宿主机器局域网IP地址或127.0.0.1

## 相关问题与解决方案

    1.如果让消息队列的Broker允许自动创建不存在的Topic？

        1.打开 broker.conf 文件，在其中找到 autoCreateTopicEnable 的设置。如果这个配置项不存在，你需要添加它。将其设置为 true

        2.配置项设置：autoCreateTopicEnable = true