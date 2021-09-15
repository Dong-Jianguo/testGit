# VN-Service - Redeureka

## 配置示例
``` 
--server.port=8762 \
--eureka.client.service-url.defaultZone=http://127.0.0.1:8762/eureka \
--logging.logpath=d://opcLogs \
--logging.level.root=info \
--spring.cloud.gateway.httpclient.websocket.max-frame-payload-length=524288000 \

```


## 配置说明

| Configuration item | Description |
| ------------------------- | ------------------------------------- |
| server.port | 服务的端口 |
| eureka.client.service-url.defaultZone |默认服务注册中心地址 |
| logging.logpath | 日志输出地址 |
| logging.level.root | 日志级别 |
| spring.cloud.gateway.httpclient.websocket.max-frame-payload-length |网关中websocket最大传输量 |

