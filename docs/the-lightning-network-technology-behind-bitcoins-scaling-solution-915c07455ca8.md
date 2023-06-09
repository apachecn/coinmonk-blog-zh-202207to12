# 闪电网络——比特币扩展解决方案背后的技术。

> 原文：<https://medium.com/coinmonks/the-lightning-network-technology-behind-bitcoins-scaling-solution-915c07455ca8?source=collection_archive---------6----------------------->

![](img/a6b5b71850076f0c9ac9ccd9a27714ac.png)

Flickr

# 介绍

众所周知，比特币每秒只能处理 7 笔交易。相比之下，VISA 通常每秒处理约 1700 笔交易，这个数字很少超过，但理论上每秒可以处理高达 65000 笔交易。

每秒 1700 笔交易，Visa 比比特币快得多，这给比特币的速度和可扩展性带来了问题。

这就是闪电网络的用武之地。

# 概述—什么是闪电网络？

闪电网络是在比特币区块链之上运行的支付协议。这是一个分散节点的网络，允许以极低的费用极其快速地发送大量交易(高达每秒一百万次)。闪电网络将交易从主要的区块链转移出来，使其高度可扩展和超便宜，使其与 VISA、MasterCard 和 Amex 等公司并驾齐驱。

Lightning Network 通过在成对用户之间建立支付通道来实现这一点，通过该通道，双方可以相互支付或接收款项。

> 交易新手？试试[加密交易机器人](/coinmonks/crypto-trading-bot-c2ffce8acb2a)或者[复制交易](/coinmonks/top-10-crypto-copy-trading-platforms-for-beginners-d0c37c7d698c)

与每笔交易都必须经过验证的主比特币网络不同，在闪电网络中，双方可以在彼此之间无休止地发送和接收资金，只有这种支付渠道的开启和关闭才会被记录在主区块链上。

![](img/0dedab88528727a483a72bf356479f2c.png)

Wheatstones

***实际例子***

爱丽丝每天早上在上班的路上都会从鲍勃的咖啡店买咖啡。由于鲍勃的咖啡店接受比特币，爱丽丝可以选择每天用比特币为每杯咖啡进行小额交易，但她必须等待 10 分钟到一个多小时才能使她的交易生效，并支付高额费用。因为爱丽丝很忙，所以她使用闪电网络。她在鲍勃的咖啡店打开支付通道，并存入价值 50 美元的 BTC，鲍勃的咖啡店创建发票，表示为 QR 码。

现在，每当爱丽丝想为她的咖啡付款时，她只需用她的 lightning 钱包扫描二维码，使她的交易即时完成，成本仅为一小部分(大大低于任何传统的支付轨道)。在这个阶段，Alice 和 Bob 的咖啡店正在彼此进行交易**离线**，在任何时候，他们中的任何一方都可以通过关闭支付通道来轻松终止这种安排。

在后台，闪电网络在爱丽丝和鲍勃的咖啡店之间创建了一个“智能合同”。

此外，为了进行交易，闪电网络不需要在每个用户之间创建支付通道。例如，Alice 的好友 Dan 来到她的社区，并且已经有了一个支付渠道。经常光顾鲍勃咖啡店的爱丽丝向丹推荐了这家店。丹现在可以通过经由爱丽丝免费发送 BTC 到鲍勃的咖啡店来每天到咖啡店购买咖啡，而不需要直接与鲍勃建立支付通道。

![](img/2b0c1959d74bb7145e54fd6d9904f119.png)

Wheatstones

***六度分隔*** —想象一下这种成倍增长，扩大到全球数百万商家，数十亿支付渠道。你可以访问一个新的国家，去购物，闪电网会想办法通过几个渠道把你和商家联系起来。这个想法是，类似于“六度分隔”的概念，所有闪电网络用户将能够直接或通过一个或多个转发用户向所有其他闪电网络用户付费。

***历史***

早在 2014 年，麻省理工学院数字计划(MIT Digital Initiative)的研究科学家 Tadge Dryja 和比特币的长期开发者约瑟夫·潘(Joseph Poon)就开始就如何扩大比特币的规模进行头脑风暴，他还与以太坊的联合创始人维塔利克·布特林(Vitalik Buterin)共同撰写了等离子白皮书。

这对搭档在 2015 年首次提出了闪电网络。他们的文章基于比特币匿名创始人中本聪之前对支付渠道的讨论。

2016 年，Dryja 和 Poon 成立了 Lightning Labs，筹集了 250 万美元，并于 2018 年 3 月推出了 Lightning Network 的测试版。

***隐私***

闪电网络增强了隐私性，因为区块链将只记录融资和结算交易，而不记录中间的任何交易。

# 引擎盖下的闪电网络

闪电网络不是区块链，而是由通过支付通道路由交易的节点维护的网络。节点由普通人和公司运行，在他们的台式机和笔记本电脑上运行程序。

**支付通道**是两人多签名地址。这意味着需要两个人的签名才能把钱取出来——类似于联名银行账户。在上面的例子中，两个用户 Alice 和 Bob 需要在他们之间建立一个初始通道来进行交易。

## 开设频道——爱丽丝和鲍勃的咖啡店

![](img/a851f5ff1c50a93062e7997955524132.png)

Wheatstones

爱丽丝通过在比特币的区块链上广播资金交易，向爱丽丝-鲍勃多签名地址汇款。之后，他们都在内部记录余额。

最初爱丽丝有 100，000 个 sat，鲍勃 0 个 sat。为了用 10，000 sats 从 Bob 处购买咖啡，Alice 将启动一个承诺事务，该事务将资金事务作为输入，向她支付 90，000，向 Bob 支付 10，000。爱丽丝和鲍勃都签署了这项交易，并各保留了一份副本——但这项具体的**交易并没有在比特币的区块链**上播出。

![](img/1f047d5a8f8512e3009208dc4881780e.png)

Wheatstones

当 Alice 第二天购买第二杯咖啡时，她创建了另一个交易来代替第一个交易，给她发送了 80，000 美元，给 Bob 发送了 20，000 美元。如果 Bob 需要为一杯咖啡退款，数字会调整为对 Alice 有利，在 Alice 的总数上增加 10，000。这些交易中没有一个与区块链有过互动，但是仍然由区块链保护**。**

如果需要，鲍勃或爱丽丝可以随时广播最新的交易，以便**从比特币区块链的支付通道**中套现，这将向他们每个人发送他们的资金份额。

## 一方消失了怎么办？

想象一下这种情况，在 Alice 向支付渠道提交资金后，Bob 立即消失，将她的资金困在需要两个签名才能将资金转移出去的多签名地址中。

为了解决这个问题，在 Lightning Network 中，Alice 会让 Bob**预先签署**一项交易，在 Alice **向主网络广播**初始资金交易之前，将所有资金发送回 Alice**。因此，即使 Bob 消失了，Alice 也会简单地广播 Bob 预先签署的退款交易来取出她的钱。**

## 一方出轨怎么办？

但是是什么阻止了 Alice 广播之前的交易呢？这些仍然是有效的、完全签名的交易，由此先前的交易可以在 Bob 给 Alice 一杯咖啡后将 90k 而不是 80k 导向 Alice？

绕过这个闪电网络包括一个聪明的方法来惩罚他们中的任何一个，如果他们通过**撤销密钥**广播一个旧的交易。每次 Alice 从 Bob 那里买咖啡，她和 Bob 都会创建一个新的事务，并且他们每个人都会交换先前状态事务的**撤销密钥，并签署最新的版本。现在，如果其中一方发布“撤销”交易，另一方可以要求欺诈者的份额，索赔者将有 24 小时的时间这样做，因为它是锁定的。**

为了避免鲍勃或爱丽丝继续监视区块链的状态，以防另一个作弊，闪电网络中有“了望塔”。**瞭望塔功能**是一种连接到另一个友好节点的机制，它为你监控你的闪电通道，防止不诚实的交易对手窃取你的资金，即使你离线。

## 通过其他渠道支付

除了个别支付渠道，如 Alice 和 Bob 之间的支付渠道，正如我们在实际例子中讨论的那样，lightning network 能够通过多个渠道发送比特币。

这是 Lightning Protocol 的亮点，因为你不必与你想交易的每个新人建立支付通道，而是可以使用网络来路由你的支付。还记得上例中 Alice 的好友 Dan 吗？他来到附近，去了咖啡店，但没有 Bob 的帐户。

让我们更详细地看一下这个例子。

![](img/8e46ac5902b791b5a9427e637536168e.png)

Wheatstones

我们有丹、爱丽丝和鲍勃的咖啡店。Dan 希望通过 Alice 向 Bob 支付咖啡费用，之前他已经与 Alice 建立了支付渠道。

![](img/37624853d326b0fdc22d67f164df141d.png)

Wheatstones

Bob 创建了一个**‘秘密’**(字节组合)和该秘密的散列，并将其作为 lightning 发票上的 QR 码与 Dan 共享。

![](img/b197b0c0e306f64d505946c8df7ba619.png)

Wheatstones

然后，Dan 与 Alice 签订了一份新合同，从她的主账户中扣除了一些资金。然后爱丽丝和鲍勃签订了一份类似的合同。

![](img/9324d41eb45e4c6a12eacf5a93c9f241.png)

Wheatstones

一旦每个人都签署了这些新的交易并撤销了以前的交易，Bob 向 Alice 透露了秘密并取消了临时合同，将余额从临时总额转移到 Bob 的主总额。然后，Alice 将这个秘密传递给 Dan，创建了一个新闻事务，取消了临时合同，并将余额转移到 Alice 的新总数中。

合同从左到右建立，暂时锁定资金，然后从右到左解锁资金，通过第二轮交易完成支付。如果 Bob 消失了，再也不揭秘，大家资金岂不是都被套牢了？

## 哈希时间锁合同(HTLC)

HTLC 是任何闪电交易的核心。这是一个超时，它被添加到所有的交易中，如果在截止日期之前没有透露秘密，则将资金返还给原始所有者。没有风险，因为要么每个人都得到报酬，要么谁都没有。

## 多种支付渠道中的隐私

Lightning 网络的多通道架构维护交易隐私。这是因为参与者没有意识到他们之前和之后的通道。他们不知道自己是在一个 5 人、10 人还是 50 人的链条中。

# 闪电网络的挑战

## 集中式集线器

使用闪电网络的小额支付渠道，比特币可以扩大到每天数十亿笔交易，然而，这只能通过使用大型、集中的“银行”中心来实现(目前)。按照目前的格式，闪电网络不会完全是点对点的。

![](img/815b09f6e67e241e2cc1459ac8711a6e.png)

flickr; Paul Baran (Network Topologies, 1964)

有三种类型的网络可以应用于资本市场

**集中的**——代表遗留的资本市场。这些是主要的交易所，如纳斯达克和大型银行，如贝莱德。

(B) **分散的中心**——较小的实体，如网上交易所和当地/地区银行。

(C) **分布式**——代表比特币的主区块链。一个完全分布式的网络，没有中间人，没有看门人。

闪电网络，如果它有任何真正的机会扩展到数十亿用户，而不是真正的点对点，将最有可能属于类别(B)。原因是，当你在闪电网络上通过多个支付渠道发送 BTC 交易时，途中的每一个多签名钱包**都必须有大于或等于发送金额的 BTC 余额**，这使得更大的交易更难进行。

此外，个人没有多少动力在闪电网络上保持支付渠道畅通。当 BTC 在不同支付渠道之间转换时，支付给任何中介机构的费用很少超过几分之一便士。可以有把握地假设，普通用户不会有大量的 BTC 被锁定，普通用户也不太可能为了几分钱的利润而将他们的 BTC 锁定在闪电网络上。

此外，如果比特币的价格上涨或崩溃，我们可能会看到许多支付渠道关闭，因为 multi-sig 参与者为了利润或由于恐慌而出售他们的 BTC，从而缩小网络的规模。

由于上述所有原因，支付应用、加密交易所和从事比特币工作的科技公司最有可能建立渠道，从而创造出一种“中枢辐射模式”。

# 街区大小——登上 LN 的世界需要 100 多年？

![](img/7ec22535589f031d344ad50bad5b3ad0.png)

flickr — stevendepolo

比特币最初被设计为点对点现金，随着块大小的增加而增加，然而块大小一直是一个有争议的话题。许多人认为，该协议的块大小上限是一个关键的保护参数，增加块大小将威胁到分散化，因为最终只有少数计算机能够存储 BTC 交易的完整历史，因为这对大多数人来说都太大了。

根据闪电网络白皮书，为了让闪电网络扩展到数十亿人，比特币块大小必须增加。参见 J. Poon 和 T. Dryja 发表的 Lightning Network 原始白皮书第 55 页，其中指出:

![](img/5ee215c83c659f4f38073c7dcb9d886a.png)

Lightning Network whitepaper

目前，以目前的区块规模，平均交易速率通常为 3 至 4 tps，为世界上每个人创建一个单一的闪电网络通道，整个比特币网络完全专用于此，将需要大约 140 年。

为什么？首先，你需要得到比特币——交易一。然后，创建闪电通道需要第二次比特币交易，之后结算通道需要第三次交易。这相当于比特币区块链上每人 3 笔交易。

由于比特币每天的最大平均交易量约为 35 万笔，这意味着每天会有超过 11.6 万人加入闪电网络(LN 为 35 万 tpd/3 txs)——假设该网络没有其他任何活动，没有常规的 BTC 交易。现在，如果我们试图搭载 60 亿人(世界成年人口)，那么以每天 116K 的速度，将需要大约 140 年才能让全球成年人口登上闪电网络。

然而，在实际意义上，它只需要一次交易，因为用户可以转换他们的菲亚特，并通过闪电网络使用中介将它直接发送出去，如北海巨妖，它有 746 个开放的直接渠道，即分散的枢纽模式。

没有必要离开闪电网络。闪电是打算用来花钱，你会经常花与商人，而不是你的生活储蓄。对于 lightning 来说，最好的情况是用户加入，然后坚持使用。离开闪电网络的唯一真正原因是，如果出现任何问题，用户需要在区块链安全地保护他们的资金。

这使我们达到每人一笔交易，或者换句话说，大约 47 年才能让 60 亿人加入闪电网络——考虑到除了让人们加入闪电之外，区块链实际上与所有其他事情都隔绝了。

为了解决这个问题，lightning 开发人员提出了一个名为**Lightning Channel factors**的概念，它将通过减少链上交易的最终数量来提高渠道管理的效率。

![](img/38ce8ba8ef87b25913bc98221a931ce7.png)

themoneymongers.com

本质上，渠道工厂只是 2 对 2 支付渠道的延伸。因此，在渠道工厂中，您可以进行资金由多方分配的 5/5 或 10/10 多 sig，而不是 2/2 多 sig。

通道工厂的概念将允许在一次交易中将多个用户装载到 lightning 网络上。对于具有 100 个组内信道的 20 个用户的组，区块链交易的成本降低了 90%。这意味着搭载 60 亿人的时间框架将缩短至 3-4 年。

# 第四维思考

比特币不是一种静态技术，而是一套不断发展的协议。它随着时间的推移而发展，同时保护其基本的货币属性及其去中心化的特质，在这种情况下，没有任何一方可以指导比特币如何发展。

想想闪电网络本身的发展。2017 年，在比特币核心中实施了隔离见证(SegWit)升级，这使得闪电网络成为比特币区块链之上的第二层。在 SegWit 被激活之前，闪电网络是不可行的，因为它严重依赖未经确认的比特币交易，因此只要交易具有延展性，就容易受到攻击。

SegWit 改进了比特币的几个方面，并为未来的升级打开了大门，其中包括一个主要的升级，称为 Taproot。2021 年 11 月上线的 Taproot 升级提供了变通办法，并消除了比特币代码中的限制，以增加网络的现实世界用例。例如，在 Taproot 之后，比特币网络转向使用 Schnorr 签名来签署交易，这减少了链上交易的规模，更快地验证了交易，并改善了隐私。

由于多种技术原因，Taproot 极大地提高了比特币闪电网络的可扩展性和隐私性(主要是改用点时间锁定合同和批量验证，这两种方式都是通过 Schnorr 签名实现的)。在 Taproot 之后，比特币闪电网络对用户来说应该会变得更加直观和划算。

比特币协议的改变就像扔进湖里的石头，导致了连锁反应。正如 Segwit 升级解决了块空间的紧迫问题，同时也通过解决交易延展性实现了闪电网络的启动，Taproot 对比特币协议的更改将产生直接影响，同时为未来的发展奠定基础。

闪电网络只是一个开始。

*免责声明:本文包含的信息仅用于教育目的，并不构成 Wheatstones 的任何形式的建议或推荐，用户在做出(或避免做出)任何投资决定时也不打算依赖这些信息。*