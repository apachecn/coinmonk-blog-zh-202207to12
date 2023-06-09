# 在区块链密码难题中寻找随机数的本福特定律

> 原文：<https://medium.com/coinmonks/benfords-law-to-find-nonce-in-blockchain-cryptographic-puzzles-300e29e107b5?source=collection_archive---------37----------------------->

> 本福德定律(也称为第一位数定律)指出，数据集集合中的第一位数可能会很小。

例如，一个集合中的大多数数字(约 30%)将有一个前导数字 1，而预期概率是 11.1%(即九个数字中有一个)。其次是以数字 2 开头的约 17.5%。这是一个意想不到的现象；如果所有前导数字(0 到 9)的概率相等，那么每个数字出现的概率为 11.1%。

该定律仅适用于有效数* S(x) (Hill 和 Berger，2017 年)，它本质上是放入标准格式的任何数字。要找到有效数:

*   找到第一个非零数字，
*   将小数点移到该数字的右边，
*   忽略这个标志。

# **用途**

本福德定律的一个实际应用是欺诈和错误检测。预计大量数字将遵循该规律，因此会计师、审计师、经济学家和税务专业人士有一个基准，即一组数字中任何特定数字的正常水平是多少。

*   20 世纪 90 年代后半期，会计师马克·尼格里尼发现，本福特法则可以成为伪造纳税申报单的有效危险信号测试；真实的税收数据通常遵循本福特定律，而虚假的纳税申报却不遵循。
*   该法律在 2001 年被用于研究希腊的经济数据，暗示该国可能操纵数字以加入欧盟。
*   庞氏骗局可以用法律来检测。不切实际的回报，如马多夫骗局所声称的，远远低于预期的本福特概率分布(弗伦泽，2015)。

# 应用它来解决加密难题，同时挖掘加密货币:

## 我们对这个谜题了解多少？

*   由于找到满足散列要求的随机随机数的概率降低，难题难度增加。这些随机选项在任何时间点从 40 亿个选项中的成功率为 0.0000000002%
*   Nonce 是唯一可变的随机数，其被识别以在区块链中提交成功的块

## 解决方案假设-

*   通过保持第一个数字不变，运行选项并移动到下一个，从最小数字到最大数字，即 1 到 9，增加找到随机随机数的概率。
    ——如 1，10，12，13，…。，1000002 等…..2,20,21,….

基于本福特定律，我们将比顺序暴力更快地获得所需散列的随机现时。

将会收集证据来支持论文。但会很高兴听到你的经历。

> 交易新手？试试[密码交易机器人](/coinmonks/crypto-trading-bot-c2ffce8acb2a)或者[复制交易](/coinmonks/top-10-crypto-copy-trading-platforms-for-beginners-d0c37c7d698c)