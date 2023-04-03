# 无常的损失不是恶魔

> 原文：<https://medium.com/coinmonks/impermanent-loss-isnt-the-boogeyman-2cbec6e56229?source=collection_archive---------32----------------------->

DeFi 是一个奇怪的空间。一方面，它绝对充满了诈骗项目，地毯拉，黑客，庞氏骗局和利用，每个人都只是猿到边缘。有些人可能会说是一个美化的赌场，但没有开放的酒吧，或至少有 50%的机会在一手 21 点中击败赌场。另一方面，我认识的一些最聪明的人，来自各行各业和全球各个角落，都沉迷于让投资银行自惭形秽的稳定游戏、收益农业、节点和贷款策略。字面意义上的单人对冲基金，其月利润会让交易机构趋之若鹜。如果你通过了 90 度学习曲线，很好地掌握了区块链、金融、记号经济学和一些耐心，你可以把一小笔钱变成一大笔财富。更重要的是，你可以让那笔小财富以银行永远无法或不愿提供给你的速度为你服务。

![](img/66b585d3e369b907330ea50fd8279da3.png)

如果这么好，为什么没有更多的人这么做？当然，这是有风险的。Crypto 并不是最成熟的领域，实现它需要时间，而且很多人需要 rekt。但也有恐惧。害怕把事情搞砸，害怕不太了解如何管理资金和掌控一切。对于经验丰富的资产经理来说，在任何市场生存都是一场斗争，不仅仅是加密，更不用说持续盈利了。然而，有一种模式我个人已经见过太多次了:对遭受无常的损失(IL)感到极度恐惧。

# 什么是无常的失去？

无论是我的一个朋友、投资银行的分析师还是网上的某个人，人们似乎都非常害怕把自己的资金输给这个看不见的代币咀嚼者。IL 是流动性提供者因其提供的资产比率因市场条件变化而遭受的暂时资金损失。它还显示了与简单地持有资产相比，提供商遭受的利润损失。

IL 影响流动性池，其中基金之间通常有 50/50 的分割(例如，提供价值 1000 美元的 ETH 和价值 1000 美元的 CRV)。每当一个代币经历价格变化时，池中的两个代币的比率改变，以保持其初始值。你总是会得到更多的贬值令牌，而更少的升值令牌。如果一个人完全瘫痪或者完全坦克化，你将会有接近 100%的非永久性损失。这是因为资金池总是会重新平衡自己，这样流动性提供者就会收回他们最初投入的资金。

通过提供流动性，参与者从每笔交易中获得费用。例如，Trader Joe 对所有交易收取 0.3%的费用，其中 0.25%进入初始池。然后，流动性提供者通过流动性池令牌(LP 令牌)获得这 0.25%的一部分，等于他们在池中的比例份额，流动性池令牌是所提供比率的代表。因此，如果一个池有价值 50.000 美元的 AVAX 和价值 50.000 美元的 JOE，并且您已经存入价值 5000 美元的 AVAX 和价值 5000 美元的 JOE，则您拥有该池的 10%份额。因此，您将从每笔交易的 0.25%费用中获得 10%，当然可以通过 LP 令牌赎回。由于两种代币的价格都是由资金池比率决定的，因此它们可能与交易所不同。套利机器人非常乐意解决这种情况。很酷吧？

![](img/d3e1dbd31ce25af7f414047cc3b7e2ac.png)

Source: TraderJoe

无常的损失实际上一直都在发生。加密是一个自由市场，有各种各样的因素使代币暴涨或暴跌。每当相对于所提供的流动性池中的其他令牌的价格发生巨大变化时，IL 接近 100%。

让我们看一个关于 MATIC(多边形)和 USDC 的实际例子，假设 MATIC 值 1 美元。我们还假设您提供了价值 1000 美元的每一种，通过提供 1000 MATIC 和 1000 USDC，使池的总价值达到 2000 美元。如果 MATIC 下跌到 0.50 美元，那么池的比率已经改变，现在您有 2000 FTM 和 500 USDC。

对于那些想为它建立一个电子表格的数据爱好者来说，这里有一个公式及其细目分类:

**IL(k)= 2k1+k — 1**

其中“k”是从初始价格到未来价格的变化率。例如，如果一项资产增值 10%，那么 k=1.1。确定“k”后，将百分比乘以初始价格，即可得到实际金额。

例如:如果 IL=0.5%，初始资产价格为 1000 美元，则实际 IL 的金额为 1000 美元* 0.5% = 5 美元。

# 它对投资组合的破坏有多严重？

很明显，几乎百分之百。既然我们已经掌握了基本知识，有一点变得显而易见:流动性提供者总是会得到更多贬值的资产，而得到更少升值的资产。利润来自于所有这些变化之间的费用。理想情况下，当用户最初存放的令牌比率=1 时，他们希望退出。也就是说和他们开始时一样。如果一项资产要么被完全抛售，要么完全贬值，流动性提供者的投资组合将遭受几乎 100%的损失，正如下面来自 dailydefi.org 的[的令人敬畏的非永久性损失计算器的例子。](https://dailydefi.org/tools/impermanent-loss-calculator/)

![](img/fe66c0ae945ee7bf5adf85f335ee2efd.png)

但是，如果无论如何都发生了，为了实际盈利，损失太大的风险不是太大了吗？不完全是。实际上，造成重大损失所需的价格变化是相当大的。当然，如果你选择提供流动性，比如说一对 BNB 和一些随机出现的硬币，后面没有流动性或白皮书，如果代币变为零，那么你的可赎回流动性池代币的价值也将变为零。

![](img/c3034a17cf21913b968bf9c7e6f0603c.png)

从本质上来说，上图告诉我们的是，与简单地持有资产相比，损失是什么:

![](img/15b557bed900c3c50bfe1586dcfd67dd.png)

尽管这肯定是一件需要时刻保持警惕的事情，但它只不过是一种在提供分散流动性时自然发生的经济现象。这是风险管理模型中需要考虑的另一个因素。

# 如何避免无常的损失

完全 100%避免它是极其不可能的。然而，如前所述，如果管理得当，提供流动性可能是有利可图的，并有助于积累选择的象征。同样，如果管理得当。否则，简单的加密或 DeFi 爱好者最好只持有某种资产。下面是一张图表，由 [Balancer](https://balancer.tools/impermanentLoss) 提供，显示了与简单持有一项资产相比，不同比率的资产池中产生的 IL。查看 Balancer 提供的链接，了解他们令人敬畏的 3D 计算器！

![](img/07114daed4499a66fc5e37ede8a0c9e3.png)

Source: Balancer

在熊市、牛市或蟹市中，提供流动性，或者更一般地说，提供高产养殖，通常有不同的做法。不言而喻，为了避免 IL，要做的第一件事就是向久经考验的强劲资产提供流动性。想想瑞士联邦理工学院、AVAX、CRV、BNB、AAVE 等等。以以太坊为例，在牛市中为以太坊和[凸](https://www.convexfinance.com/)的 CVX 代币提供流动性，这是一个针对[曲线](https://curve.fi/)的收益率优化平台，将会产生以下结果:不仅提供商暴露于两种随市场攀升的资产，CVX 也与以太坊密切相关，并与其生态系统保持一致。每当有人在这个池中进行交换时，提供者持有的两种资产都会增加。即使考虑到 IL，如果提供商在 ETH 和 CVX 的比率与存款时大致相同时退出头寸，他将有效地渴望市场并拥有更多这两种资产，这两种资产的美元计价价值也有所增加。

熊市则不同。流动性提供者可以长期看好某项资产，比如说 AVAX，但短期看跌，并希望积累该资产。实现这一点的一个方法是在一个可变/稳定的池中提供流动性。让我们以 AVAX/USDC 为例。1 美元兑换= 1 美元，尽管市场条件不佳(当然，除非发生大规模的 depeg 事件)。随着理论上的熊市发挥作用，拉低资产价格，提供商的 LP 令牌比率将改变，以增加 AVAX，从而损害 USDC。再加上常规复利，你会有更多的 AVAX。本质上，形象化这种现象的最简单的方法是理解它就像是在你想要积累的代币上进行 DCA-ing。令人惊讶的是，退出头寸的理想时机是当 AVAX 的价格回升到 LP 令牌创建时的价格时。

![](img/914346f7f09c5af631a281070f594264.png)

Source: Alpaca Finance

这两种方法都适用于螃蟹市场，收益工艺既是一门科学也是一门艺术，还有 LP 对冲这种东西，然而在动荡的市场中，还有其他更具资本效率的资金管理方法。显然不是财务建议。

# 结束语

如上所述，白细胞介素不是一个可怕的夜魔。理解它，解释它，并将其应用到您可能使用的任何风险管理模型中。未知往往是可怕的，直到它被理解。在那里保持安全，负责任地耕作，不断学习！

> 交易新手？试试[加密交易机器人](/coinmonks/crypto-trading-bot-c2ffce8acb2a)或者[复制交易](/coinmonks/top-10-crypto-copy-trading-platforms-for-beginners-d0c37c7d698c)