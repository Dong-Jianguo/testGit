# VN-Service - Vn_event

## 配置示例
``` 
--server.port=8155 \
--spring.shardingsphere.datasource.master.url="jdbc:mysql://127.0.0.1:3306/network_udpn_vn2" \
--spring.shardingsphere.datasource.master.username=username \
--spring.shardingsphere.datasource.master.password=password \
--spring.shardingsphere.datasource.slave.url="jdbc:mysql://127.0.0.1:3306/network_udpn_vn2" \
--spring.shardingsphere.datasource.slave.username=username \
--spring.shardingsphere.datasource.slave.password=password \
--besu.node.url=http://127.0.0.1:8083/besu \
--besu.contract.attempts=50 \
--besu.contract.sleepDuration=1000 \
--besu.UDPN_BASIC_MEMBER_NODE_LOGIC=0xFD91E0b48787A75f2CC76eF412ceDEd075e2AE11 \
--besu.UDPN_BIZ_MEMBER_NODE_LOGIC=0xcA1968841412603b76077d9ae8DA641a761cDc9A \
--besu.UDPN_BALLOT_BASIC_MEMBER_NODE_LOGIC=0x790B3e4D0A9BF53D7A6fAfd0524a46A2C145926B \
--besu.UDPN_BALLOT_BIZ_MEMBER_NODE_LOGIC=0xB4299D7596529fF8dF496e53fFD77944bCCA3AE1 \
--besu.BALLOT_STRATEGY=0x1A6ED901CCE9e9A36940A3cC3d432b127B7edBa6 \
--besu.UDPN_PAYMENT_TRANS_LOGIC=0x620f34A905eB4937514B6C393B6c73c6B01e62Af \
--besu.EXCHANGE_RATE_STRATEGY=0x4436Dc9d9bf786143afF85f86429702413e0a1D3 \
--besu.UDPN_SERVICE_FEE_LOGIC=0xEb4C48e34543c2C8FC34db6C22b867aEF25B35Cd \
--besu.UDPN_BALLOT_SERVICE_FEE_LOGIC=0x645F92E6CF1102d8418DACFA426881a480F66cdA \
--eureka.client.service-url.defaultZone=http://127.0.0.1:8762/eureka \
--spring.vn-code=VN2222 \
--spring.rabbitmq.host=127.0.0.1 \
--spring.rabbitmq.virtual-host=vhost \
--spring.rabbitmq.mgrport=15672 \
--logging.logpath=d://opcLogs \
--logging.level.root=info \

```


## 配置说明

| Configuration item | Description |
| ------------------------- | ------------------------------------- |
| server.port | 服务的端口 |
| spring.shardingsphere.datasource.master.url |主数据库地址 |
| spring.shardingsphere.datasource.master.username |主数据库用户名 |
| spring.shardingsphere.datasource.master.password |主数据库密码 |
| spring.shardingsphere.datasource.slave.url |从数据库地址 |
| spring.shardingsphere.datasource.slave.username |从数据库用户名 |
| spring.shardingsphere.datasource.slave.password |从数据库密码 |
| besu.node.url | besu节点地址 |
| besu.contract.attempts | 连接besu失败后重试次数 |
| besu.contract.sleepDuration | 重试间隔时间 |
| besu.UDPN_BASIC_MEMBER_NODE_LOGIC | 节点管理合约地址 |
| besu.UDPN_BIZ_MEMBER_NODE_LOGIC | 节点业务管理合约地址 |
| besu.UDPN_BALLOT_BASIC_MEMBER_NODE_LOGIC | 节点信息投票合约地址 |
| besu.UDPN_BALLOT_BIZ_MEMBER_NODE_LOGIC | 节点业务信息投票合约地址 |
| besu.BALLOT_STRATEGY | 投票策略合约地址 |
| besu.UDPN_PAYMENT_TRANS_LOGIC | 交易合约地址 |
| besu.EXCHANGE_RATE_STRATEGY | 汇率合约地址 |
| besu.UDPN_SERVICE_FEE_LOGIC | 服务费合约地址 |
| besu.UDPN_BALLOT_SERVICE_FEE_LOGIC | 服务费投票合约地址 |
| eureka.client.service-url.defaultZone |默认服务注册中心地址 |
| spring.vn-code | vn的唯一code |
| spring.rabbitmq.host | rabbitmq地址 |
| spring.rabbitmq.virtual-host | 连接虚拟mq地址 |
| spring.rabbitmq.mgrport | rabbitmq端口 |
| logging.logpath | 日志输出地址 |
| logging.level.root | 日志级别 |

