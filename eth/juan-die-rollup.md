# 🧻 卷叠(Rollup)

将数百笔交易打包（或“卷叠”）到一层网络的一项交易中。这会将一层网络的交易费分散到整个卷叠中的所有用户，降低每个用户的费用。

## 乐观卷叠

假定交易是有效的，但可以在必要时提出质疑。如果交易被怀疑无效，则会运行一项错误性证明，验证是否已经发生无效交易。

{% embed url="https://ethereum.org/zh/developers/docs/scaling/optimistic-rollups/" %}

## 零知识卷叠

使用有效性证明，其中的交易是脱链计算的，然后将压缩数据提供给以太坊主网，以证明其有效性。

{% embed url="https://ethereum.org/zh/developers/docs/scaling/zk-rollups/" %}
