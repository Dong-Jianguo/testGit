# VN-Service - Vn_base_server

## 配置示例
``` 
--server.port=18021 \
--spring.shardingsphere.datasource.master.url="jdbc:mysql://127.0.0.1:3306/network_udpn_vn2?characterEncoding=UTF-8&useSSL=false&serverTimezone=Asia/Shanghai" \
--spring.shardingsphere.datasource.master.username=root \
--spring.shardingsphere.datasource.master.password=Red80@80 \
--spring.shardingsphere.datasource.slave.url="jdbc:mysql://127.0.0.1:3306/network_udpn_vn2?characterEncoding=UTF-8&useSSL=false&serverTimezone=Asia/Shanghai" \
--spring.shardingsphere.datasource.slave.username=root \
--spring.shardingsphere.datasource.slave.password=Red80@80 \
--eureka.client.service-url.defaultZone=http://127.0.0.1:8762/eureka \
--email.host=smtp.exmail.qq.com \
--email.user=xxxxx@xxxx.com \
--email.password=xxxxx \
--email.from=xxxx@xxxx.com \
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
| eureka.client.service-url.defaultZone |默认服务注册中心地址 |
| email.host | 邮件服务器地址 |
| email.user | 邮件服务用户名 |
| email.password  | 邮件服务密码 |
| email.from | 邮件服务发件人 |
| logging.logpath | 日志输出地址 |
| logging.level.root | 日志级别 |

