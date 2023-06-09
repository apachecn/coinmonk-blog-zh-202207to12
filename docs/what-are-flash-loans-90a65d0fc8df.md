# 什么是闪贷？

> 原文：<https://medium.com/coinmonks/what-are-flash-loans-90a65d0fc8df?source=collection_archive---------37----------------------->

***闪贷是几个流行的 DeFi 协议的一个功能，允许你在不需要抵押品的情况下借入加密货币资产，条件是债务在同一笔交易中偿还。我们能相信它吗？有风险吗？一起看看吧！***

![](img/5b83a765ba5b5a9c00d74948e7282e80.png)

快速贷款已经成为 2020 年**分散金融世界中最重要的发展之一，给一些市场参与者带来利润，同时给其他人造成损失。**

# **闪贷是怎么出现的，什么时候出现的？**

自从分散贷款开始以来，所有的加密资产贷款都要求借款人提供额外的担保(抵押品)。这种情况在 2020 年 1 月发生了变化，总部位于英国的贷款公司 Aave 推出了基于流动性池的分散式贷款协议。第三方 DeFi 开发商获得了即时无担保贷款。

![](img/f1393f11c7044d888f2f5d4b5464635e.png)

快速贷款的基本要求很简单:贷款发放和还款交易，以及任何支付资金的中间操作，都必须发生在单个交易块中。这样一来，从借款到还款的时间只有几秒钟。同时，即时贷款的规模可以达到数千万美元，佣金仅为金额的 0.09%(除了解决智能合同的天然气成本)。

在 Aave 关于即时贷款的文档发布后，DeFi-application 开发者几乎立即意识到了这一功能的巨大潜力。然而，几个月后，随着 DeFi-application 用户数量的增加和以太坊网络上佣金的增加，它变得非常受欢迎。传统的 DeFi-protocol 交易非常昂贵，而基于即时贷款的策略的使用大大节省了成本，并发现了新的收入机会。

Aave 的借贷平台在 2020 年**年底处理了 20 亿美元的闪付贷款，到 2021 年**上半年**结束时，这一数字已经上升到 42 亿美元。据 AaveWatch 报道，最大一笔即时贷款为 1.95 亿美元。**

在 2020 年上半年，分散交易平台 dYdX 的用户可以使用闪贷功能。flash swaps 功能是由流行的分散式加密货币交易所 Uniswap 在 v2 协议版本中于 2021 年 5 月**推出的，可以被认为是即时贷款的一种模拟。**

用户可以在不提供任何抵押品的情况下借用 100 多个令牌，这些令牌可用于套利交易(例如 Uniswap 和 SushiSwap 之间)和其他策略。此功能只能通过智能合同访问，因为没有用户界面。借贷成本为 0.3%(不包括汽油费和 Uniswap 佣金)。

# **什么时候可以用闪贷？**

获得低成本无担保贷款的能力为 DeFi 用户创造了大量从市场低效率中获利的机会，同时也降低了贷款和其他操作的成本。下面列出了使用快速贷款最常见的情况。

***套利交易***

从一种资产在不同交易大厅的差价中获利需要使用大量的自有资金。根据以下计划，即时贷款成为此类业务的低成本融资来源:

*   从 DeFi-protocol 获得给定资产的快速贷款；
*   用借来的资金购买更便宜的 DEX 上的资产；
*   在 DEX 上卖出资产，因为它更贵；
*   用费用和利息偿还 flash 信用。

套利交易是使用 flash credits 的最常用场景。

***债务头寸的自我清算***

当抵押品的价值低于借款人的债务价值时，贷款协议会启动自动清算程序。出售部分抵押品以偿还债务，并评估清算罚款，在 Aave 上为 [5%或 10%](https://docs.aave.com/risk/asset-risk/risk-parameters) (取决于抵押品的类型)，在金库服务 MakerDAO 的情况下为 13%。

使用即时贷款可以让你做一个更便宜的自我清算没有罚款，而不必等待这个昂贵的程序，通过使用以下方案:

*   对资产进行快速贷款；
*   用借入的资金偿还债务，从而释放保证金；
*   使用部分保证金，以适当的费用和利息偿还闪贷。

***快速更换抵押物***

当抵押资产价值下降或清算风险上升时，可能需要更换贷款抵押品。在这种情况下，谨慎的做法是将下跌的资产换成上涨或波动性较小的加密资产。

传统的抵押品置换要求全额偿还债务，然后重新开放，这增加了交易费用，并需要获得全部债务。通过将所有交易合并在一个区块链中，flash credits 让您可以更快、更便宜地完成交易。

***快速贷款再融资***

各种 DeFi 平台的贷款利率根据市场状况和可用流动性而波动。事实证明，快速贷款是一种有用的工具，可以将低成本贷款“翻转”到较低利率的平台，包括用另一种资产替换抵押品。

# **闪贷有多危险？**

不仅是开发者和密码交易者，就连攻击者也开始利用即时贷款。2020 年 2 月，针对 DeFi-protocols 的两次闪贷攻击导致了 100 万美元的损失。他们利用了 bZx 协议中的一个缺陷，该协议允许他们操纵加密货币价格，并人为抬高价格以获利。即时贷款本身没有漏洞，但它们为攻击提供了非常廉价的资金来源。

在 **2020** 中，快速信用攻击是从各种 DeFi 协议中窃取资金的最常见方法之一。大多数攻击都利用了与所用定价预言的不可靠性和操纵资产价格的能力有关的漏洞。

在 **2021** 的春天，即时贷款在多个 EVM 支持的网络上同时可用，引发了一系列的 DeFi-protocol 攻击，最明显的是币安智能链(BSC)网络。

2021 年 5 月，由于 BSC 网络受到攻击，分散服务总共损失了 1.67 亿美元。亏损最大的是 Belt Finance 项目(5000 万美元)和 Pancake Bunny(4500 万美元资产)。BurgeSwap、ApeRocket、bEarnFi 和其他一些基于 BSC 的 DeFi 项目也是受害者。

> 你有什么想法？如果你有什么要补充的，请在下面留下你的评论！
> 
> 在[媒体](/@SunflowerCorpAdmin)或[推特](https://mobile.twitter.com/sunflower_corp)上关注[向日葵公司](https://sunflowercorp.com/)定期更新趋势加密新闻。

![](img/8c571db8f50a1ea82567d3de13f95703.png)

[*向日葵公司*](https://sunflowercorp.com/) *—专注于最佳交易体验和卓越技术的新型加密货币衍生交易所。*

我们提供杠杆高达 x100 的 BTC/USDT 永久期货，以及最具趋势性的工具。当您与我们交易时，您将获得一个可定制的交易终端、各种图表、技术分析工具、各种订单类型以及“止损”和“获利”订单选项。

> 交易新手？试试[加密交易机器人](/coinmonks/crypto-trading-bot-c2ffce8acb2a)或者[复制交易](/coinmonks/top-10-crypto-copy-trading-platforms-for-beginners-d0c37c7d698c)