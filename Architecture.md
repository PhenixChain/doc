**V1 架构分析**

1.节点类型

1）Client

2）Peer ：

（1）Endorser 对客户端的请求进行判断 ，在此处执行chaincode，也就是智能合约实现

（2）Committer 接受Orderer的共识结果，进行账本改变

3）Orderer

（1）Consenters 共识批准，接受来自Endorser认可后Client传来的信息，并将共识结果传给Peer的Committer节点进行提交

**如图：**

**client**

\|    \|

\|    \|（1）\[这里client请求执行合约，改变账本,属于双向操作，peer执行完智能合约返回结果\]

\|    \|

\|    \|------**endorsing**（peer1）------\|

\|    \|------**endortsing**（peer2）-----\|

\|    \|------**endorsing**（peer3）------\|

\|                                                     \|

\| （2）\[传给Orderers合约结果\]  \|

\|                                                     \|

**Orderers**-----------------------------------\|（3）\[确定合约结果，达成共识\]

\|

\|（4）\[将确定的合约结果传给一个peer进行committing\]

\|

**Committing**\(Perr\)



