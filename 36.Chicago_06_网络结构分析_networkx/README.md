# 36.Chicago_06_网络结构分析_networkx
网络结构（图）可以辅助分析数据间的联系关系，尤其在社交网络数据分析上，能够发现Node之间的关联，这个Node可以是待分析的任何数据类型，例如人及其社交属性，
地理空间及其属性等。而Edge则是Node之间的联系桥梁，表示Node之间连接的属性强度，例如人人之间的交流程度，区域间的距离程度等。在此次实验中则分析Chicago公园系统内，各个公园在空间上的距离关系，联系程度。在计算上关键使用两个库，其一为网络里结构图networkx，用于建立网络图结构；其二为pysal库，用于计算距离权重。依据计算的距离权重来建立网络图，发现公园空间分布上的关系。

同时，为了更加方便的观察网络结构中，提取联系紧密的区域，距离权重大于96%部分，最大边，与长度大于10（°）的值。可以依据计算的结果，进一步分析公园分别的特点，以及与城市环境之间的关系。

在计算公园边界形式指数的过程中，使用sympy库来书写公式，其结构清晰。初步计算SHAPE，FRAC, S,L等基本指数，并用boxplot箱型图统计分析结果。
# 计算结果
## 基本统计
SHAPE，FRAC, S,L等基本指数公式书写与计算。boxplot统计分析。
![](https://github.com/richieBao/python-urbanPlanning/blob/master/images/36_01.png)

## 距离权重网络结构graph
其中Node为公园中心点位置，大小代表面积。edge为前93%，具有较大距离权重的值，线的粗细为距离权重大小。
![](https://github.com/richieBao/python-urbanPlanning/blob/master/images/36_02.png)

## 网络结构的边
提取了在距离权重大于96%部分，最大边，与长度大于10（°）的值
![](https://github.com/richieBao/python-urbanPlanning/blob/master/images/36_03.jpg)
