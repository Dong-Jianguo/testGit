# VN-Service - Vn_did

## 配置示例
``` 
--server.port=8042 \
--eureka.client.service-url.defaultZone=http://127.0.0.1:8762/eureka \
--spring.vn-code=VN0002 \
--did.properties.file=/did_vn/application-besu.properties \
--logging.logpath=d://opcLogs \
--logging.level.root=info \

```


## 配置说明

| Configuration item | Description |
| ------------------------- | ------------------------------------- |
| server.port | 服务的端口 |
| eureka.client.service-url.defaultZone |默认服务注册中心地址 |
| spring.vn-code | vn的唯一code |
| did.properties.file | DID SDK配置文件地址 |
| logging.logpath | 日志输出地址 |
| logging.level.root | 日志级别 |

