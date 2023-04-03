# 你需要知道的关于 zkEVM 的一切

> 原文：<https://medium.com/coinmonks/everything-you-need-to-know-about-zkevm-4c6698144684?source=collection_archive---------10----------------------->

就像在所有技术的生命周期中一样，区块链的采用与它整体面临的障碍相关。很长一段时间以来，整个领域面临的最大挑战之一是解决方案的可扩展性。

许多解决方案试图解决这个问题，但是，同时也产生了一个减少分散化的附带问题。从 2020 年夏天到 2022 年的牛市期间，直到崩溃费用，采用率是递增的，这进一步说明了这一点。

虽然市场达到了危险的高点，但汽油费也提高了过高的数额。更重要的是，它发生得太频繁了。其中一个潜在的原因是，项目上线的网络和用户交易的网络之间缺乏区分；一个部门 web2 受益于 web3，而这正是 web 3 所缺乏的。

零知识以太坊虚拟机，顾名思义，就是生成零知识证明来验证数据的正确性，进而验证程序的正确性的虚拟机。它们基本上是以太坊之上的一层；ZK 汇总向以太坊提交交易数据和零知识证明，以验证离线交易批次的有效性。

![](img/c605cb8787806aea28c2ac02b8a7e49b.png)

**什么是 ZK 汇总？**

简而言之，汇总在链外执行事务计算，但在链上存储事务数据；在数据中创建两个层。这是通过智能合约处理的，智能合约的主要功能是捆绑交易数据，并将其转移到链外进行处理。然后，这由网络上的参与者处理，这些参与者被称为“验证者”或“定序者”，他们随后提交包含验证交易所需的最少信息的成批数据。

这就是 ZK 卷与乐观卷不同的地方。ZK 汇总生成用于验证交易有效性的加密证明。另一方面，乐观汇总假设所有事务都是有效的，并且不执行任何有效性检查。

**什么是 ZK-EVM？**

简单来说，以太坊虚拟机(EVM)是以太坊执行其事务的机制。这个想法是，每个区块链都需要一个机制来确保事务是有效的，因为每个块中的每个事务都意味着机器的状态发生了变化。

以太坊的想法是让一台全球计算机通过单独的节点连接起来。EVM 就是那个网络。EVM 基本上是一个生态系统中各种活动发生的环境。

对于习惯于在 Ethereum 环境中工作的开发人员或用户来说，不适当的状态改变至少会引起麻烦。它很有可能使应用程序完全不可用。

这里的想法是在保留以太坊所有功能的同时，以不损害环境完整性的方式扩展以太坊的功能。至少可以说，这是一个复杂的问题。

理想情况下，这意味着汇总的环境应尽可能靠近 EVM，然而，在靠近 EVM 的增量与成本之间存在显著的正相关关系。Vitalik Buterin 也指出了这一点(由 Polygon 总结):“zkEVM 的每个细节越接近 EVM，生成 ZK 证明的成本就越高”

zkEVM 将以太坊环境复制为一个 rollup，并允许开发人员像在以太坊上一样进行构建。这个想法是开发人员不需要改变他们的代码或放弃他们的 EVM 工具，而走向一个汇总。

Vitalik Buterin 按照与以太坊的接近程度，将上卷分为四种类型:

类型 1-zkEVMs:完全等同于以太坊
zk-EVM 类型 1 将完全等同于以太坊，在它们的共识内，它们的状态或事务树实际上没有改变。type-1 zkevm 与 EVM 完全兼容，但需要更多的时间，因为没有重新工作来使证明生成更快。

**2 型 zkevm:EVM 等效物**
2 型 zkevm 的目标是“像”以太坊，在拥有相当于 EVM 而不是以太坊的原生环境方面。它们外表看起来像以太坊，但是它们的 EVM 进行了修改，使得证明生成过程更快。

**第三类 zkevm——脱离以太坊**
第三类 zkevm 专注于在 zk-rollups 内创建类似 EVM 的系统。这意味着要对 EVM 进行特定的更改，以使构建应用程序更容易，证明生成过程更快。然而，一些用本地 EVM 链构建的应用程序可能需要重新布线。

类型 4 zkEVM——衍生 EVM
zkEVM 类型——4 可以用于高级语言，但不能用于 EVM 本身。这里的过程有几个层次，通过跳过为 EVM 执行的每个阶段提供零知识证明的过程而变得高效。

**结论**

zkEVMs 是区块链互补产品系列中的最新产品。如前所述，该空间作为一个整体面临的最大问题之一是，尽管是分散的，区块链技术是不可扩展的。

主要投资公司已经开始意识到这类产品的价值。Scroll、Polygon 和 zkSync 目前正在竞争推出他们的产品；尽管还在进行中，但我确信它们只是一长串工作的开始。

*最初发表于*[*【https://www.codezeros.com】*](https://www.codezeros.com/blog/everything-you-need-to-know-about-zkevm)*。*

> 交易新手？尝试[加密交易机器人](/coinmonks/crypto-trading-bot-c2ffce8acb2a)或[复制交易](/coinmonks/top-10-crypto-copy-trading-platforms-for-beginners-d0c37c7d698c)