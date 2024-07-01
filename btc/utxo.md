# 📑 UTXO

## Base

**UTXO（未花费交易输出）模型**

将每笔交易构成包含一个或多个不同的输入和最多两个输出（一个用于支付，另一个返回任何可能的零钱给发送者），每笔交易都会花费之前交易的输出，并生成可供未来交易使用的新输出。

在任何时间点，我们都有所有“未花费交易输出“的完整记录。这种存储和跟踪未花费交易的模型称为UTXO模型。

**用户的钱包会跟踪与用户拥有的所有地址相关的未花费交易列表。**

它记录交易事件，而不记录最终状态。

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

* 每个 UTXO 的历史都可以追溯到 coinbase 交易的一个或多个输出
* 每个区块中的第一笔交易是 coinbase 交易。&#x20;

交易费不以交易输出（UTXO）的形式体现。它是通过Input和Output之间的差额推算得出。

## UTXO set

UTXO 集合是给定时间点存在的所有 UTXO 的综合集合，该集合中每个 UTXO 数量的总和就是该时间点现有比特币的总供应量。

比特币作为一种货币的特殊之处在于，任何人都**可以随时以无需信任的方式验证总供应量**，所有节点都维护 UTXO 集的相同副本，当创建新块时，UTXO 集会随着一些 UTXO 的使用和新 UTXO 的创建而更新。

## UIB

**UIB (UTXO ISOMORPHIC BINDING)**

利用UTXO模型的同源特性，通过“一次性密封”的方式，可以将目标链A的UTXO映射到另外一条图灵完备的UTXO链B上。

代表协议：**RGB++** by CKB

用开发的术语，其实就是一个中间件，让原本不具备图灵完备特性的 Bitcoin 在其他链上散发更多可能性。
