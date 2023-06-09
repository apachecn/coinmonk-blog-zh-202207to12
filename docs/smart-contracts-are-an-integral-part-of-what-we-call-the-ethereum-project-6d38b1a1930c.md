# 智能合约是我们称之为以太坊项目的一个组成部分

> 原文：<https://medium.com/coinmonks/smart-contracts-are-an-integral-part-of-what-we-call-the-ethereum-project-6d38b1a1930c?source=collection_archive---------41----------------------->

![](img/71d098bb5ce0e590c1ffc8e60a772917.png)

Smart contracts

对于那些没有读过或听说过这个术语的人来说，智能合同是一段代码，可以由各种系统运行，以执行无信任协议。智能合同的运作原则是，如果一方根据商定的条款和条件付款，那么他/她将获得权利。该系统不需要任何人工干预(完全自动化)。

智能合约的概念是由 Nick Szabo 在 1994 年首次提出的。Szabo 是一名计算机科学家、法律学者和密码学家，他将自己描述为“合法的无政府主义者”(他将此解释为相信国家无法无天，但法律仍然有助于创建社会秩序的人)。

智能合约是我们称之为以太坊项目的一个组成部分。该项目始于 2013 年，2015 年正式发布。但是在进入正题之前，让我们快速的讨论一下以太坊到底是什么…

# 以太坊:快速概述

正如已经指出的，以太坊只是一个基于区块链技术的开放软件平台。该平台提供了一种称为“Solidity”的图灵完全编程语言。这意味着可以编写既安全又高效的代码。

以太坊使用户能够在区块链上执行智能合约。可以通过单一界面查看、编辑、测试和调试合同状态。使用以太坊，不再需要从头开始创建应用程序。相反，它可以使用现成的组件使某些操作更容易实现(例如，有一个 Oracle 组件使验证各种操作的结果变得更容易)。这也使得程序员可以利用现有的库来创造新的东西。

以太坊可以用来做各种事情。然而，它最适合开发和运行本质上是分散的应用程序(因为区块链技术已经允许这样做)。

# 以太是什么？

很多人错误地把以太坊和以太混为一谈。这是可以理解的，因为这两个术语总是可以互换使用。但是它们的意思不一样。简单地说，以太坊代表一个平台，而以太是一种加密货币，为这个平台提供燃料。

以太是由 Vitalik Buterin(以太坊项目的主要开发者)在 2013 年推出的，从那以后越来越受欢迎。以太是使用以太坊平台的必备部分。这是客户为软件执行的各种任务支付的一种形式。

乙醚最初用于法定货币交易，如美元和欧元。然而，很快就可以使用以太购买其他加密货币，如比特币和莱特币。

> 交易新手？试试[加密交易机器人](/coinmonks/crypto-trading-bot-c2ffce8acb2a)或者[复制交易](/coinmonks/top-10-crypto-copy-trading-platforms-for-beginners-d0c37c7d698c)

# 智能合同基础

智能合约是一个可以在以太坊区块链节点上运行的程序。一旦满足某些条件，就可以触发智能合约中包含的代码；这些条件是在编写智能合同代码本身时确定的(它们保存在区块链中)。

该程序可以触发各种效应——它可以向其他合同发送信息并修改区块链(例如通过在链中添加新区块，甚至删除或更改旧区块)。

让我们看一个简单智能合约的例子。假设你有一辆车。您决定要卖掉那辆车，因此您为该交易创建了一个智能合同:

您为这个智能合约编写代码，并将其上传到区块链。任何人在网上都能看到这份合同。有人过来决定买你的车，于是他向你的智能合约代码中列出的钱包地址发送以太币(或其他货币)。智能合同检测到它已收到付款。现在你的车是他的了，钱包里的钱也收到了。

# 智能合约现已完成。

在任何人向您发送 Ether 作为付款之前，他或她将确保满足所需的条款(他/她将确信代码正确工作)。一旦出现这种情况，就可以付款了。支付完成后，智能合约将执行其所有编程任务，如其代码所述。智能合同的一个常见例子是车祸保险索赔。

比如智能合约上写着发生了事故，要求车主索赔。智能合同现在可以确定是否满足任何条件(例如，它检查汽车是否损坏)。如果一切顺利，付款的一方将从他们的保险公司得到一笔赔付。

以太坊智能合约的另一个常见用途是管理数字令牌(包括货币等现实世界的资产)。为了使这成为可能，有必要对不同的加密货币进行某种分散的交换。

以太坊的主要目的之一是为平台上的资产创建一个去中心化的交易所。

以太坊虚拟机可以以两种模式之一运行智能合约:它可以完全离线运行，也可以在线运行。如果智能合约在线运行，那么它的代码可以被其他人访问，例如平台的其他用户和其他应用程序(它以纯文本形式可见)。相比之下，脱机智能合约没有这种可能性，其代码受到加密保护。

# 智能合同是如何工作的？

智能合同的工作方式与您计算机上的任何程序大致相同。这意味着契约必须有一定数量的内存可供其执行。这种存储器被称为 RAM(随机存取存储器)。

在以太坊的情况下，这个 RAM 是由以太坊块组成的。以太坊块是一种存储区块链状态的文件类型，存储在网络中的所有节点上。如果智能合约需要修改存储在以太坊块中的数据，那么它只需要能够修改该块中的一个字节。为此，它将使用一条名为“OP_CHECKDATASIG”的指令，该指令可用于从区块链上的另一个块中读取一个字节。

以太坊虚拟机有 256 字节的可用 RAM，足以存储以下值:

一个字节。

最大 1024 字节的文档。

一种最大 2048 字节(指令)和 256 字节(堆栈元素)的程序。

一个 16 位整数或一个下溢的 32 位整数。请注意，整数总是以小端字节顺序存储，这意味着最不重要的字节将首先存储。这意味着 0x 0123456789 abcdeffedcba 9876543210 将被存储为:0x deedcba 9876543210 ABC 0123456789。

我们设想，智能合约可能想要在块中写入一个地址，以便稍后可以从区块链中检索该地址的余额。有 256 个可能的地址，因此这将需要一个智能契约来存储高达 256 位的数据。

当然，这意味着写入一个块至少需要 256 字节的 RAM，因此存储的数据量取决于写操作的时间。例如，如果只需要写两个字符——A 和 B——那么我们可以使用这些数学运算将它们存储为 2 个字节:A XOR B。

在区块链中修改数据被称为“删除”数据，这比写入一个字节需要更多的 RAM。因此，要存储 256 位的数据，我们还需要再分配 256 字节的 RAM。

有关智能合约如何在以太坊网络中工作以及它们如何相互交互的更多信息，请查看以下资源:

# 以太坊 P2P 网络基础

如前所述，以太坊的创建是为了让人们能够进行去中心化的应用。可能有人创建了一个智能合同，提供了一个销售汽车或购买房屋的系统。这些都是真实世界的应用程序已经全面展开的实际场景。

作为一个分散的应用程序，智能合同将在区块链上运行，不需要任何第三方。这意味着它只能通过两种方式与其他节点通信:

# 通过使用 IP 地址。通过使用其他智能合约。

IP 地址—公有地址和私有密钥

以太坊节点运行在世界的不同地方，在不同的计算机上。例如，可能有一个以太坊节点在纽约运行，另一个在莫斯科运行，还有一个在新德里运行；它们都是通过公共互联网连接的。每个节点必须有一个唯一的 IP 地址，这样它才能与网络上的其他节点通信。

每个节点都用自己的 IP 地址作为公有地址，可以随便叫。可以想象，这只对从网络上的其他节点接收输入消息有用。如果一个消息由一个节点发送到另一个节点，那么发送者和接收者通过他们的 IP 地址就可以知道。

私钥也可以用来接收消息:它允许访问特定的以太坊帐户。与公共地址不同，在公共地址中，每个人都可以看到彼此的 IP 地址，这个密钥只能由拥有正确密码的密钥持有者使用。例如，密码可能允许某人从他们的钱包向另一台计算机上的指定帐户汇款(这将被视为身份管理)。

# 智能合约是在区块链上达成的交易

使用以太坊智能合约有一个你可能没有考虑到的关键方面:在一个节点上发生的事情不可避免地也会在网络中的其他节点上发生。这意味着，如果智能合约将数据写入数据块，那么每个节点都会见证这一事件，并同意将数据存储在那里。如果两个不同的智能合约将一条消息(或任何内容)写入同一个块，那么每个人都会看到这两条消息。

这可能是一个优势，原因有几个:如果你想建立一个应用程序，多方可以设置规则，允许彼此之间自动付款，那么区块链技术将是这个目的的完美选择。

举个例子:想象三个人想玩一个游戏，但是只有一个人能赢。这将是非常简单的事情:三名球员将各自开设一个新的帐户，他们都列为合同的所有者。这意味着，在从他们的任何账户转移任何资金之前，他们都必须同意。玩家可以就他们想要的任何规则达成一致，例如将有多少回合以及每回合他们将得到多少分。

此外，任何智能合约都可以创建一个单独的智能合约，它可以使用自己的规则独立运行。这意味着智能合约可以作为一个游戏独自运行，只有它自己的规则(而不一定是其他玩家的规则)。一个智能合约可以用于保存每一轮的所有数据，而另一个智能合约用于允许从一个帐户向另一个帐户付款；这两个契约可以通过多种方式协同工作。

一个简单的例子可能是，一个智能合同是托管服务:它持有资金，直到所有要求的条件都得到满足。第二智能合约是第一智能合约和第二智能合约之间的协议。第一个智能合约可以将资金释放给另一方，而第二个智能合约允许资金从一个账户转移到另一个账户。

另一个简单的例子是智能合约，它有自己的规则，保存你的密码，这样你就可以访问你的数字钱包。这样你就可以从你的电子钱包中转账，而不需要第三方(比如交易所)。

任何人都可以创建自己的区块链，在其上他们可以运行任何他们想要的规则。这使他们能够完全控制如何在区块链中读写数据。

我们现在已经看到了以太坊是如何工作的，也了解了不同类型的智能合约。

关于以太坊网络和它的功能还有很多信息要介绍，但是我们会在以后的文章中介绍。到目前为止，希望这是一个有趣的介绍，足以解释区块链技术，让您了解它是什么，以及如何在现实世界中使用它。

请记住，这不是关于加密货币及其价值的教程；互联网上有许多其他资源进一步讨论了这些主题。然而，它的目的是帮助你理解以太坊是如何工作的，这样你就可以开始在以太坊网络上进行开发。

请关注有关以太坊网络、智能合约和加密货币的更多帖子。我们将从不同的角度详细讨论这些主题:从它们的创建到它们所支持的技术的应用，以及它们如何在以太网上工作。

如果你想更深入地了解区块链技术，那么可以考虑阅读我们的免费电子书《区块链技术终极指南》。它将让您很好地了解区块链技术，并为我们的一些文章提供背景。

要了解更多关于区块链技术的信息，请查看我们的区块链终极指南和我们的区块链课程。这些将帮助你理解技术的基础，以及如何在以太坊网络上使用它。

摘要文章名称了解以太坊——概述描述区块链技术和以太坊的初级读本:以太、智能合约和创建区块链的简单介绍。作者詹姆斯·克拉克出版社名称 tech project 出版社徽标