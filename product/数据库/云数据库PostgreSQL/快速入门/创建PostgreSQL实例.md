本文为您介绍如何通过 PostgreSQL 控制台创建实例。

## 前提条件
已 [注册腾讯云账号](https://cloud.tencent.com/register?s_url=https%3A%2F%2Fcloud.tencent.com%2F)，并 [完成实名认证](https://console.cloud.tencent.com/developer)。

## 操作步骤
1. 登录 [PostgreSQL 购买页](https://buy.cloud.tencent.com/pgsql)，根据需求指定数据库实例信息，确认无误后，单击**立即购买**。
 - **计费模式**：支持包年包月和按量计费。
 - **地域**：实例实际部署的地域；建议与需要对接的云服务器保持一致，以便延迟最低。
 - **可用区**：在同一地域内电力和网络互相独立的物理数据中心；建议与需要对接的云服务器保持一致，以便延迟最低。支持多可用区部署（主节点和备节点位于不同可用区）和单可用区部署（主节点和备节点位于同一可用区），具体主备可用区选择以实际购买页为准。
 - **网络类型**：实例所处的网络，建议与需要对接的云服务器保持一致，以便延迟最低。
>?私有网络：是用户在腾讯云上建立的一块逻辑隔离的网络空间，在私有网络内，用户可以自由定义网段划分、IP 地址和路由策略。
>
 - **架构**：云数据库 PostgreSQL 默认支持双机高可用（一主一从）的架构。
 - **数据库版本**：PostgreSQL 的不同数据库内核版本之间存在功能差异，详见：[10](https://www.postgresql.org/docs/10/static/index.html)、[11](https://www.postgresql.org/docs/11/index.html)、[12](https://www.postgresql.org/docs/12/release-12-4.html) 、[13](https://www.postgresql.org/docs/13/index.html) 的官网介绍。
 - **数据库内核版本**：详细介绍请参见 [内核版本概述](https://cloud.tencent.com/document/product/409/67018)。
 - **实例规格**：实例规格代表不同的性能水平和价格基数。
 - **硬盘**：默认采用 SSD 盘（本地盘）。
 - **备份空间**：免费赠送购买实例容量的50%，超过免费容量部分，目前免费。
 - **实例名**：可选择创建后命名或者立即命名，仅支持长度小于60的中文、英文、数字、`_`、`-`。
 - **字符集**：云数据库 PostgreSQL 支持字符集 UTF8 和 LATIN1。
 - **用户名**：帐号名需要1个 - 16个字符，只能由字母、数字或下划线组成；不能为 postgres；不能由数字和 pg\_ 开头；所有规则均不区分大小写。
 - **密码**：密码长度8位 - 32位，推荐使用12位以上的密码，不能以`/`开头，必须包含以下所有项目：
     - 小写字母 a - z
     - 大写字母 A - Z
     - 数字 0 - 9
     - 特殊字符 `()~!@#$%^&*-+=_|{}[]:;'<>,.?/`
 - **指定项目**：如果您期望不同团队管理不同数据库，请指定到不同团队所处的项目中。
 - **安全组**：一种有状态的包含过滤功能的虚拟防火墙，用于设置单台或多台云数据库的网络访问控制，是腾讯云提供的重要的网络安全隔离手段。
 - **标签**：便于分类管理实例资源。
 - **购买数量**：指一次性可购买的实例个数，为避免误操作，我们设置了一次购买上限10个，如果您期望购买更多个数，请多次购买。
 - **购买时长**：由于采用包年包月的模式，您需要预估数据库期望使用时长。
 - **服务条款**：阅读并勾选，详细请参见 [云数据库服务条款](https://cloud.tencent.com/document/product/409/39115)。
2. 购买完成后，返回 [实例列表](https://console.cloud.tencent.com/postgres)，待实例状态变为**运行中**，即可进行连接操作。

## 后续操作
您可以使用标准的 SQL 客户端，通过内网地址或外网地址连接到云数据库 PostgreSQL，请参见 [连接 PostgreSQL 实例](https://cloud.tencent.com/document/product/409/40429)。
