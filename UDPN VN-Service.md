# UDPN VN-Service

## What is VN-Service?
The Validator Nodes are at the heart of the UDPN. Any transaction on the UDPN will be validated by a cluster of Validator Nodes which are connected with all the other stakeholders via a secure and encrypted connection. The Validator Nodes and TAR Nodes are the only ones which store the full set of transaction data on the UDPN. Transaction Nodes are owned and operated exclusively by the UDPN Alliance members. 

It must be noted that a Validator Node only validates the format of the message received from a certified Business Node. Upon receipt of a message, the Node validates the veracity of the signature and message origin. It does not however validate the content of the message. The content is only validated by the currency systems, depending on the nature of the transaction.  Each transaction submitted from the Business Nodes will be randomly assigned to certain Validator Nodes to validate. All transactions are validated and written to the peer of Validator Node which reads, endorses, and writes transactions to the distributed ledger Blockchain ledger. The Validator Nodes are connected to the Business and Transaction Nodes through secure APIs.

Each Validator Node’s operations are conducted with full autonomy. The UDPN has no controlling entity but is governed by means of a majority voting. All the Validator Node owners will have the right to vote on such topics as network access permissions, the performance of software updates, the approval of new smart contract deployment and adjustments to fee structures. 

<div align="center">
<img src=./vn.png />
</div>

All Validator Nodes contain a governance system that ensures adherence to the rules of the UDPN. As there will be multiple Validator Nodes in the network, with more being added as the alliance grows, not all Validator Nodes are required to participate in the same transaction.

Validator Nodes should be installed in the members’ own cloud account or on-premises infrastructure. As part of the Validator Node installation, each member will also install the UDPN governance software.      

## Known issues
- 包名使用小驼峰式命名法进行命名


## 项目模块
- comp-api-model:vn项目的公用实体模块。
- comp-common:vn项目的公用方法模块。
- comp-besu:vn项目请求besu模块。
- comp-did:vn项目关于did操作的模块。
- chaingateway：vn项目的网关，对外提供给BN。
- redeureka:vn项目的注册中心。
- vn_control:vn项目关于权限操作的模块，目前包括投票相关操作。
- vn_member:vn项目关于成员节点操作的模块，目前包括节点入网、服务费入网、业务信息入网相关操作。
- vn_did:vn项目关于操作DID Document的模块，目前包括DID验签、上链相关操作。
- vn_base_server:vn项目基础服务模块，目前包括发送邮件服务。
- vn_event:vn项目的事件监听服务，目前包括监听链上交易。
- vn_init:vn项目的初始化模块，目前包括初始化数据库。

## 前置条件
### 1.模块启动顺序
redeureka->chaingateway->vn_init->vn_base_server->(vn_control、vn_member、vn_did、vn_event)

首先启动注册中心提供注册服务；然后启动网关服务；再启动vn_init，初始化数据；再启动vn_base_server获取基础服务；最后启动 vn_control、vn_member、vn_did、vn_event（无顺序）。

## Quick Start

克隆项目后获取源码jar，可以通过以下两种方式启动项目，**注意各模块启动顺序**。

- 直接使用命令行启动项目，启动配置项参考各模块下的README.md
`java -jar xxxxxx.jar --server.port=8151 --spring.vn-code=xxx`

- 通过创建shell脚本启动项目，启动配置项参考各模块下的README.md

1，在jar包同目录下创建shell脚本

`start`

```
#!/bin/bash     
nohup java -Xms256m -Xmx512m -jar `pwd`/xxxxxx.jar \
--server.port=8155 \
--spring.vn-code=xxxxx \
 > log.log  2>&1 &
tail -f ./log.log

```

`stop`

```

#!/bin/bash     
PID=$(ps -ef | grep `pwd`/xxxx.jar  | grep -v grep | awk '{ print $2 }')
if [ -z "$PID" ]
then
    echo Application is already stopped
else
    echo kill -9 $PID
    kill -9 $PID
fi

```

2，执行shell脚本
启动项目
`./start`
停止项目
`./stop`

## contact us

Email: xxxx@reddatetech.com