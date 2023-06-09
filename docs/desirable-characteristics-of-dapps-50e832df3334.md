# dApps 的理想特性

> 原文：<https://medium.com/coinmonks/desirable-characteristics-of-dapps-50e832df3334?source=collection_archive---------57----------------------->

![](img/00296ef5552ca87eb916bd50e0746f04.png)

Photo by [Shubham Dhage](https://unsplash.com/@theshubhamdhage?utm_source=medium&utm_medium=referral) on [Unsplash](https://unsplash.com?utm_source=medium&utm_medium=referral)

区块链技术在学术界和资本市场都引起了极大的关注。然而，对数千种可用加密货币和众多初始硬币发售骗局的铺天盖地的猜测也带来了对这一新兴技术的臭名昭著的辩论。本文追溯了区块链系统的发展，揭示了分散应用的重要性和区块链的未来价值。我们调查了最先进的 dapp，并讨论了区块链的发展方向，以满足 dapp 的理想特性。读者将获得 dApp 研究的概述，并熟悉区块链的最近发展。

未来的 dApps 要求区块链平台满足以下理想特性:

# A.更好的性能

## 1)低延迟

自比特币诞生以来，长时间的交易延迟一直是一个关键问题。由于比特币节点挖掘一个区块的平均时间为 10 分钟，平均交易确认时间约为一小时(因为用户通常会等待 6 个区块)。尽管以太坊中的响应延迟已经显著降低到 15 秒左右，但支持一般应用程序交互的足够小的延迟仍有待实现。事实上，更长的延迟让用户感到沮丧，并使 dApps 与现有的非区块链替代品相比竞争力下降。例如，基于区块链的社交网络网站中的普通用户通常会要求系统在 2 到 3 秒内对他/她的喜欢做出响应或分享对帖子的操作。

## 2)高吞吐量

现代基于网络的系统，例如社交网络、大型多人在线游戏、在线购物中心，需要区块链平台来支持每天数百万的活跃用户。因此，处理大量并发流量的能力在 dApp 平台中至关重要。然而，当前的区块链平台仍然受到吞吐量瓶颈的困扰。例如，CryptoKitties 在推出时获得了很大的人气，一度占以太坊所有交易的近 30%，这导致了约 30，000 个待处理交易的峰值积压。

## 3)快速顺序性能

在系统设计中，软件组件或逻辑步骤之间的依赖关系限制了应用程序的执行。某些应用程序中的某些过程，如对某一特定数据的更新，由于顺序依赖于前面步骤产生的结果，因此不能并行实现。在区块链系统中，dApp 的连续性能由网络中所有节点的响应延迟决定，因为所有事务/操作都应该由所有节点执行和验证以达成一致。因此，托管 dApps 的区块链平台需要快速的顺序性能来处理大量数据。

# B.启用离线交易

许多当前的区块链系统依赖于互联网连接来快速验证资金。参与特定区块链网络的系统可能会定期脱机。然而，如果设备的子集与互联网断开连接并相互交换签名的交易，那么如果具有与离线设备相同的密钥对的另一个保持在线的设备具有同时消费的能力，则不能保证不会发生双重消费。例如，考虑一群人带着他们的移动电话乘公共汽车去一个偏远的村庄。这个村庄没有互联网接入。dApp 可以被设计成使得它可以接受为支付商品而签名的离线交易。公共汽车上的人可以通过这种方式使用本地蓝牙连接将他们购买椰子的付款发送给供应商。当这个签名最终在稍后时间被转发到互联网时，支付将是成功的，除非公共汽车上的人也在他们的家用计算机中使用相同的密钥对，并且在他们离线之前花掉了钱。当大量设备分散网络时，这个问题变得更加复杂。由于许多区块链依赖于超过 51%的设备进行协作，因此可能存在潜在的恶意攻击，攻击者可以战略性地攻击互联网基础设施，以便利用 51%的攻击进行分而治之[32]，[33]。

# C.合理的货币成本

## 1)交易费用低

作为对区块生产商激励的一部分，交易费的概念伴随比特币诞生。在经典的区块链系统中，例如以太坊，交易费也可以是防止垃圾邮件或恶意执行智能合约的一种方式，因为入侵者需要花费他们的令牌来开始他们的攻击。然而，由于交易间接费用的比例很大，交易费成为货币价值相对较小的交易的障碍。在当前的区块链生态系统中，dApp 开发者正在努力应对他们在部署和执行智能合同时需要支付的高额交易费。

## 2)现代免费互联网商业模式

与交易费相关的另一个关键问题是商业模式。默认情况下，动作发起者，例如以太坊中智能合约的调用方，需要在使用系统之前购买令牌。这限制了 dApp 的用户基础，特别是因为加密货币尚未在社会上获得普遍接受。事实上，现代互联网商业模式是基于用户流行度的快速增长，这意味着 dApp 开发者应该具有向用户提供免费服务的灵活性。换句话说，用户不需要购买或持有令牌来使用平台，这导致了更广泛的采用。未来的 dApp 可以采用现代互联网商业模式，向用户提供免费服务，并与用户和内容制作者分享平台利润。

# D.柔性维修性

## 1)支持系统升级

由于区块链技术仍处于起步阶段，区块链系统不可避免地需要从一个版本升级到下一个版本。然而，由于 P2P 共识的性质，硬分叉是当前区块链系统自我升级的唯一途径，这可能导致参与网络节点的丢失。硬分叉的另一个潜在问题是，将有多个相似的令牌共享一个共同的原点，这将使用户感到困惑。比如像比特币和比特币现金一样，2016 年 7 月‘以太坊’(ETH)和‘以太坊经典’(ETC)互相分叉。为此，下一代区块链系统需要一种系统升级机制，以便于对部署在其上的 dApps 进行版本控制。

## 2)易于错误恢复

智能合同中的安全问题已经在许多以前的工作中进行了研究[34]-[36]。虽然大多数错误和系统缺陷可以通过仔细的实现和密集的测试来防止，但几乎不可能保证一个重要的智能契约没有错误。一些 dApps 的高度复杂性加剧了这种情况。然而，区块链数据的不可变性质阻止了对 dApps 的修改，这使得不可能交付 bug 补丁。因此，区块链平台必须为 dApp 开发人员提供支持错误恢复方法的灵活性，特别是对于那些可能破坏 dApp 中整个生态系统的关键问题。

# E.更简单的身份管理

许多区块链 dApp 系统都面临着身份方面的挑战。一些系统如 ZCash27 和 Monero28 试图隐藏用户和交易的身份。最近还在现有区块链的基础上增加了匿名功能，特别是在初始硬币发行(ico)等用例中，资金是通过智能合同筹集的，监管机构要求了解您的客户(KYC)和反洗钱(AML)检查[37]，而无需向整个全球网络提供捐助者的身份。另一方面，有一种趋势是创建一个通用身份，如 Blockstack29，它可以跨所有 dApps 使用，就像 openID30 用于跨 web 服务创建通用身份一样。

…………………………………………………………………………………………………

**参考文献**:[https://IEEE explore . IEEE . org/abstract/document/8466786/references # references](https://ieeexplore.ieee.org/abstract/document/8466786/references#references)

> 交易新手？试试[密码交易机器人](/coinmonks/crypto-trading-bot-c2ffce8acb2a)或[复制交易](/coinmonks/top-10-crypto-copy-trading-platforms-for-beginners-d0c37c7d698c)