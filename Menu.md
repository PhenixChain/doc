# 源码目录

builds：用于内核升级，运行go build命令。

cmd：命令行工具

* benchcore：测试性能
* blockcache：？块的缓存
* corectl：设置core模块参数
* cored：core服务
* decode：解码工具
* deploy：部署
* ed25519：ed25519非对称加密工具
* gobundle:遍历目录下的文件
* gobytes：打印字符串为字节流操作
* hex：十六进制编解码操作工具
* md2html：md转换成html工具
* metricsd：内核运行健康状态监控
* migratedb：数据库迁移
* multitool：cmd下集成命令工具
* perfdash：性能监控
* sha3：sha3哈希
* shake：sha3哈希的扩展
* slashland：？？
* testbot：？？测试
* testnet-info：测试网络信息
* testnet-reset：测试网络返回
* varint：varint编码
* vet：go代码错误检查工具

core：核心

* accesstoken：操作token。Client token和network token
* account：账户操作
* asset：资产
* blocksigner：块签名
* config：配置
* coretest：核心测试
* coreunsafe：警告操作（用于重置链）
* fetch：抓取链中的数据以及当前块链
* generator：生成区块
* leader：用于节点消息广播
* migrate：数据迁移
* mockhsm：模拟生成公钥私钥
* pin：区块高度状态更新
* query：实现对区块接口数据的查询
* rpc：http客户端请求
* signers：签名
* txbuilder：
* txdb：
* txfeed：



