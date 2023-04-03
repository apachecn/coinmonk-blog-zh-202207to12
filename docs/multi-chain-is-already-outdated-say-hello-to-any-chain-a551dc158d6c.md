# 多链 DeFi 是 1.0。现在向任何人问好

> 原文：<https://medium.com/coinmonks/multi-chain-is-already-outdated-say-hello-to-any-chain-a551dc158d6c?source=collection_archive---------30----------------------->

rhino.fi 刚刚向全球最大的区块链之一 BNB 智能链(BSC)引入了无摩擦跨链掉期。现在，您可以从第二层钱包中访问 250 多种新令牌，而无需复杂的网桥、网络交换机或本地令牌气费。

但是在这次最新的整合背后还有一个更大的故事。在这里。

多链被认为是 DeFi 的最终归宿。但事实上，我们还有很长的路要走。

目前有 1000 多家区块链，提供从资产和非金融资产到分散抵押贷款和令牌化股票的各种服务。而今天的多链平台只提供了其中一小部分的访问权限。

这还不够好。无论如何，不是为了 DeFi 和我们想要建立的未来。

在过去的菲亚特世界里，你的银行限制你只能获得有限数量的产品和服务，*由他们的合作伙伴提供*，而*则提供符合特定标准的*。他们选择什么时候给你机会，什么时候把你锁在外面。

DeFi 应该比银行更好:这是关键所在。但是，如果我们只给你一定数量的链，一定数量的可能性，那么我们真的没有多大的改善。

因此，我们需要一个系统，使我们能够添加任何链。一个让我们能够随时添加热门新链和机会的系统。

**这就是我们新增 BSC 的真正令人兴奋之处。它证明了我们可以以双倍的速度添加新的区块链，而不会牺牲安全性或用户体验。**

我们的多链系统依赖于不同链上的一系列‘前哨’。

我们不会在这里深入探讨(我们将把深入探讨留到另一篇文章中)，但是，总结一下，这里是它是如何工作的。

1.  我们使用 solidity smart contracts 建立了前哨——这是一种总部位于区块链的程序，使用“if>then”逻辑自动执行交易(换句话说，当满足特定标准时，合约会触发一项行动)。
2.  这些契约使我们能够代表用户执行元事务。用户在交易链外签字，我们完成交易，支付汽油费。
3.  我们的可扩展性合作伙伴 StarkEx 提供了车轮的中心，为资金转换创造了渠道。因此，你在一条链上出售一项资产，在 StarkEx 上获得你想要的资产，并可以用这项资产在另一条链上进行交易和互换。

这是一个非常创新的结构，因为你根本不需要与个体区块链互动，或者在他们之间架起一座桥梁。

事实上，我们认为我们是第一个不需要原始链的本地令牌就能实现跨链交换的项目，因为我们为您支付了汽油费。

以前，如果你想用蛋糕(BSC 目前最热门的代币之一)换 USDT，你需要持有 BSC 的本地代币 BNB 来支付汽油费。然而，使用 rhino.fi，我们将代表您支付 BNB 费用，并在我们执行互换的正常费用基础上增加该费用。

但是这种结构的另一个关键特征是它是为速度和可重复性而设计的。也就是说，可以快速应用到其他链条上。

当我们为我们的第一个多链扩展项目 Polygon 构建这个堆栈时，构建花了三个多月的时间:我们必须编写智能合同，并测试一切，这非常耗时。

但是有了 BSC，我们能够重用现有代码，并向现有合同添加简单的配置文件。这意味着我们已经能够将流程缩短到仅仅 **30 天**。

因为所有的代码都是可重用的(没有特定于任何一个链的代码),我们会变得更快。

**我们认为可以将建造时间缩短到一周。事实上，我们认为我们最终可以在 24 小时内增加一个新的区块链。**

这将使我们能够建立一个真正的多链生态系统:第 1 层 DeFi 链，第 2 层项目，侧链和 alt。我们希望将所有与 EVM 兼容的连锁店添加到我们的平台上，并且远远不止于此。

更重要的是，这将使我们能够在他们最活跃的时候提供机会。

即使区块链只存在了几个小时，我们也可以跳出来支持它——并确保你在它们消失之前得到最好的机会。

顺便说一下，这并不是要贬低 BNB 智能链的重要性。这对我们来说本身就是一个巨大的进步:我们将一个真正庞大的链带到了我们的平台上，并开放了对 crypto 中最具活力的生态系统之一的访问。对于作为用户的你来说，这意味着巨大的可能性。

但对我们来说，不仅仅是我们要去哪里。这是我们接下来要去的地方。

我们正在超越多链枢纽。我们正在成为一个链条中心。

*这篇文章是由 rhino.fi 的开发人员撰写的。请关注我们，在*[*rhino . fi Labs*](https://medium.com/u/23e55dca4488?source=post_page-----a551dc158d6c--------------------------------)*获取更多的链更新。而如果你想开始交换 BSC，多边形或者常规的 ERC-20 代币，点击* [*这里*](https://app.rhino.fi/swap?symbol=ETH:USDT) *。*

> 交易新手？尝试[加密交易机器人](/coinmonks/crypto-trading-bot-c2ffce8acb2a)或[复制交易](/coinmonks/top-10-crypto-copy-trading-platforms-for-beginners-d0c37c7d698c)