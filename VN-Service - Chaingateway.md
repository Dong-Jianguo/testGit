# VN-Service - Chaingateway

## 配置示例
``` 
--server.port=8083 \
--vncontrol.ribbon.listOfServers=http://127.0.0.1:8152 \
--vnmember.ribbon.listOfServers=http://127.0.0.1:8151 \
--vndid.ribbon.listOfServers=127.0.0.1:8041 \
--vnbaseserver.ribbon.listOfServers=127.0.0.1:18021 \
--besu.ribbon.listOfServers=http://127.0.0.1:8545 \
--besuwebsocket.ribbon.listOfServers=http://127.0.0.1:8546 \
--eureka.client.service-url.defaultZone=http://127.0.0.1:8762/eureka \
--spring.cloud.gateway.httpclient.websocket.max-frame-payload-length=524288000 \
--ribbon.eureka.enabled=false \
```


## 配置说明

| Configuration item | Description |
| ------------------------- | ------------------------------------- |
| server.port | 服务的端口 |
| vncontrol.ribbon.listOfServers | vn_control实例地址 |
| vnmember.ribbon.listOfServers | vn_member实例地址 |
| vndid.ribbon.listOfServers |vn_did实例地址 |
| vnbaseserver.ribbon.listOfServers |vn_base_server实例地址 |
| besu.ribbon.listOfServers |besu实例地址 |
| besuwebsocket.ribbon.listOfServers |besu的websocket地址 |
| eureka.client.service-url.defaultZone |默认服务注册中心地址 |
| spring.cloud.gateway.httpclient.websocket.max-frame-payload-length |网关中websocket最大传输量 |
| ribbon.eureka.enabled |是否启用eureka |

