## 一. 背景

>  最近JNS社区出现了一些诉求：希望将JNS从元码链跨到以太坊生态去；为了能够快速的验证这种诉求的合理性，我们先行采用人工桥的方式，在两条链上进行JNS的转移；待诉求的合理性经过充分验证后，可以采用更加去中心化的跨链方案；

## 二. 人工桥的思路概述

1.JNS从元码链跨到以太坊生态

   > a. 用户联系JNS DAO社区委员会，提出跨链诉求；
   >
   > b. 用户先行将jns转入一个支持NFT资产的多签合约地址；该多签合约由JNS DAO进行部署及管理；
   >
   > c. JNS DAO 社区委员会，确认用户jns转入后，在以太坊链上为用户铸造相同的jns；

2.JNS从以太坊生态跨回到元码链

   > 1. 用户联系JNS DAO社区委员会，提出跨回元码链诉求；
   > 2. 用户先行将jns资产，在以太坊生态燃烧销毁；
   > 3. JNS DAO社区委员会，确认用户已经在以太坊生态销毁jns后，将相应的jns从多签合约地址转出至用户地址；

## 三.已有的源码

> 1. JNS合约
> 2. 多签钱包合约

## 四. 待开发的内容点

1.将JNS合约扩展出burn的能力

> a. 新增burn对外接口；nft owner可以自主销毁自己的jns，不可以销毁非owner的jns资产；
>
> b. 待销毁的jns必须是unbind状态，否则无法销毁；
>
> c. 针对销毁的jns，要在合约内记录该nft的owner及销毁区块高度；

2.扩展多签钱包合约，使其支持NFT资产

> a. 不可以破坏掉已有的原生资产多签能力；
>
> b. 不可以破坏合约已有的安全性；
>
> c. 新增针对NFT的发起 “资产转移” 接口；
>
> d. 新增针对NFT的签名“资产转移” 接口；

## 五. 补偿参考

> 预估参考：  15个有效工作小时 (或3个工作日)



