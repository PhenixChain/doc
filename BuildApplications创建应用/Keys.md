# Keys键对

    introduction简介

- 加密私钥是区块链（blockchain）中的主要授权机制。秘钥控制了资产的发行（issuance）和转让（transfer）。每笔发行（issuance）或转让（transfer）交易使用特定的私钥来签署，并使用已有的公钥或资产类型来检查签名，确定新交易的有效性。
- 在示例中，资产或账户只定义单个秘钥用于发行（issuance）或转让（transfer）。但在实际环境下，可以为不同的使用模型定义多个密钥来实现不同的安全级别。例如，可以用两个签名密钥来定义更高价值的资产，需要两个不同的当事人来签署密钥确定此次发行（issuance）或转让（transfer）。联合账户也可以有两个密钥，只需要其中一个密钥你就可以签署发行（issuance）或转让（transfer）。所需要签名的人数称为法定人数。
- 在生产环境中，私钥只会在HSM（硬件安全模块）中生成。其对应的公钥被链核心使用。在区块链（blockchain）中创建的发行或转让的交易都需要在HSM中进行签署。HSM对事务进行签名，而不会泄露私钥。签名成功，事务就会被提交到区块链上。
- 对于开发环境，区块链提供了一种方便的Mock HSM。Mock HSM API与生产环境中的真实HSM API相同，可提供从开发到上线的无缝过渡。需要注意的是，Mock HSM并没有真实HSM的安全性。





    Overview概述

本指南将指导您完成基本的keys操作：

- Create key（in the Mock HSM）在Mock HSM中创建key
- Load key （into the HSM Signer）加载秘钥 进入HSM签名者
- Sign transaction （with the Mock HSM）签名交易 使用Mock HSM



    Sample Code示例代码

本指南中的所有代码示例都可以在单个可运行的脚本中查看。

- java
- Ruby



    