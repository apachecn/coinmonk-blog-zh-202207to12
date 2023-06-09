# 用 zk-SNARK 证明分散存储网络上的数据

> 原文：<https://medium.com/coinmonks/attesting-to-data-on-decentralized-storage-using-zk-snark-6b3af13134bb?source=collection_archive---------15----------------------->

假设您想证明分散存储上的数据的可靠性，但不想暴露您的身份。(实际上，这些数据是公开的，**比如你发布给所有人看的推文或论坛帖子**。)

在这篇文章中，我将提出一种使用 zk-SNARK 来实现这一点的方法。

首先，证明者将在一个分散的存储器上发布他们的数据，带有秘密的散列 *s* 和数据标识符 *id :*

*h = hash(s，id)*

数据标识符将是附加在数据上的随机值。(例如，当使用 Arweave 作为存储器时，标识符可以被设置为 Arweave 事务的标签。)

秘密 *s* 应该是可以导出证明者身份的密钥。这可能是以太坊地址的私钥。但是 dapp 不可能直接使用用户的私钥来生成证明，所以在实际使用中需要稍微调整一下。以下是更多相关信息。

接下来，证明者将创建一个证明来证明以下两个:**他们的声誉和他们对数据的所有权。**

电路将如下所示:

**私人输入**

*   密钥: *s*

**公共输入**

*   数据标识符: *id*
*   附加到数据的散列: *h*

**检查**

*   *h=hash(s，id)*
*   deriveIdentity(s)是例如人性证明集的默克尔根的一片叶子

声誉可以通过几种方式来证明，如使用 Merkle 树的 zk 包含证明，或 zk 负声誉。

通过**证明附加到数据的散列的前映像的知识来完成对上传到分散式存储器上的数据的所有权的证明。**

因为只有身份的拥有者才能构造一个 hash 使得 *h = hash(s，id)，*模仿是不可行的。

# 签名是秘密

使用以太坊钱包签名作为秘密，该方案可以变得更加实用。使用钱包的私钥作为秘密是不可行的，因为今天的标准规定 dapps 不应该能够直接访问钱包的私钥。

这需要一个由秘密签名散列组成的集合。

在创建证明之前，证明者需要通过提交秘密签名的散列来加入证明集。

# 我正在进行的工作

基于我在这篇文章中解释的方案，我目前正在开发一个 [zk 调查应用](https://github.com/DanTehrani/zk-survey)。

需要一种类似于 Typeform 或 Google form 的调查工具，但它是 web3 的原生工具。我认为一个具有分散架构并集成到其他 web3 服务的调查工具将会满足很多人(尤其是 Dao)的需求。此外，这种带有 zk 组件的工具，我相信会产生关于 zk 应用程序的见解，这对这个领域是有价值的。

其他可能继承“匿名但可信”属性的应用创意包括论坛、社交网络或举报平台，仅举几例。

# 评论

这个帖子是为了寻求反馈，所以请随时回复相关的工作，批评，想法的扩展等。

> 交易新手？试试[加密交易机器人](/coinmonks/crypto-trading-bot-c2ffce8acb2a)或者[复制交易](/coinmonks/top-10-crypto-copy-trading-platforms-for-beginners-d0c37c7d698c)