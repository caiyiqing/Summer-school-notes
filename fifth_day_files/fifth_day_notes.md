# 2019浙江大学可视化暑期学校 - 第五天
## 课程：树图与网络可视化
#### 讲师简介：周志光，浙江财经大学副教授，软件工程系主任，浙江省高校青年英才计划获得者。毕业于浙江大学CAD&CG国家重点实验室，主要研究方向为数据可视化、可视分析、经济数据分析与挖掘等。
#### 课程简介：本课程主要介绍了层次结构数据和网络数据的可视化方法并比较其优势和缺点，结合周老师自身参与的项目实例介绍了可视化开发设计的常用方法。此外，还介绍了可视化设计中的一些工具软件。

<div align=center><img width="800" height="500" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/fifth_day_files/fifth_day_notes/5-1.jpg"/></div>
<p align=center size="16">图5-1课程内容概要<p>

  
### 一、层次数据可视化
#### 层次数据的定义
层次数据的定义:即侧重于节点、数据、以及对象之间的层次关系的数据。包括社会关系、信息组织和逻辑结构等
* 层次数据举例：公司结构层次可视化
<div align=center><img width="800" height="500" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/fifth_day_files/fifth_day_notes/5-2.jpg"/></div>
<p align=center size="16">图5-2公司结构层次可视化<p>
  
 #### 层次数据的可视化方法
 层次数据可视化方法主要有三种：**节点链接图、空间填充法、混合法。**
 * **节点-链接型**：包括正交布局、圆形布局。正交布局包括电路图、缩进图和树形图，圆形布局包括径向树和双曲树。电路图的优点是正交且节省空间，缺点是对电脑友好，但对用户不友好。缩进图的优点易于实施，可以应用于纯文本或HTML，缺点是大数据浏览需要大量滚动，而且可能会丢失上下文。比起正交布局，圆形布局的空间利用率更高。圆形布局缺点：当数据属性特别多或数据分布不均匀时时会导致某些数据分配的空间特别小。
 <div align=center><img width="800" height="500" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/fifth_day_files/fifth_day_notes/5-3.jpg"/></div>
<p align=center size="16">图5-3节点-链接形可视化方法<p>
  
  **节点链接法实例**
将数据属性抽象为树状结构，根据树状结构之间的关系投影到二维平面的散点图；为了找出多元图中节点之间存在的多维属性信息，通过邻接关系构成树状结构进而构建层次关系和对应邻接矩阵来观察特征信息。
 <div align=center><img width="800" height="500" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/fifth_day_files/fifth_day_notes/5-4.jpg"/></div>
<p align=center size="16">图5-4英国财政可视化<p>
  
 * **空间填充法**：空间填充法中主要以层次结构为主。采用矩形表示层次结构里的节点，父子节点之间的层次关系用矩形之间的相互嵌套隐喻来表达，这种方法可以充分利用所有的屏幕空间。
 <div align=center><img width="800" height="500" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/fifth_day_files/fifth_day_notes/5-5.jpg"/></div>
<p align=center size="16">图5-5伦敦个人住房交易可视化<p>
  
  * **混合法**：节点链接法能清晰、直观地显示层次结构，而空间填充法能有效地利用空间，从而支持大规模的层次数据，将两者结合，可以结合双方的优势，但缺点是产生的可视化结果相对复杂。**每个方法适用的场景不同，下图给出了各种方法在不同场景下的性能。**
  <div align=center><img width="800" height="500" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/fifth_day_files/fifth_day_notes/5-6.jpg"/></div>
<p align=center size="16">图5-6树图扩展方法在各方面性能分析<p>
 
#### 家谱数据可视化案例
* 数据源：来自中国多代人口数据库（CMGPD-LN），拥有1749-1909年辽宁省700个村庄中260,000名当地居民的150万条记录。
* 分析任务：整个家庭或一代人的人口特征？随着时间的推移家庭迁移行为的变化过程和迁移行为的原因？如何找到家庭进化中的具体模式？世代之间的生殖关系是否平衡以及如何量化它？空间分布与家庭属性之间的关系？
<br>**可视化效果如下**
  <div align=center><img width="800" height="500" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/fifth_day_files/fifth_day_notes/5-7.jpg"/></div>
<p align=center size="16">图5-7家谱数据可视化界面<p>
  
 ### 二、网络数据可视化
 #### 网络数据的定义
 网络数据的定义：树型结构表达了层次结构关系，与树形可视化中的层次结构相比，网络数据呈现出更加复杂和灵活的关系。如：社交网络、移动网络、邮件网络、协作网络等
<div align=center><img width="800" height="500" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/fifth_day_files/fifth_day_notes/5-8.jpg"/></div>
<p align=center size="16">图5-8移动专利诉讼关系（网络数据）<p>
 
 #### 网络数据的可视化方法
 网络数据可视化方法分为三种：**节点链接图、邻接矩阵和混合法**。
 * **节点链接图**
 <br>包括Sugiyama适用于内在有序图形，图形深度可以映射到轴。特点：1、高可读性，2、快速（取决于启发式方法）3、没有内在顺序的图表不太好，4、易于实施[graphviz](http：//www.graphviz.org)
 
<div align=center><img width="800" height="500" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/fifth_day_files/fifth_day_notes/5-9.jpg"/></div>
<div align=center><img width="800" height="500" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/fifth_day_files/fifth_day_notes/5-10.jpg"/></div>
<p align=center size="16">图5-10节点连接图举例<p>
  
 * **邻接矩阵**
<br>邻接矩阵是一个N×N矩阵，表示N个对象之间的关系。 •位置（i,j）表示第i个和第j个对象之间的关系。邻接矩阵法的缺点是对于间接关系，也就是关系传递性的可视表达比较薄弱，而且可视化结果也比较抽象，不易于观察者理解。
<div align=center><img width="800" height="500" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/fifth_day_files/fifth_day_notes/5-11.jpg"/></div>
<p align=center size="16">图5-11 邻接矩阵示意图<p>
 
 * **混合方法**
 节点链接布局适用于节点规模大但边关系较为简单的情况，邻接矩阵适用于节点规模较小，但边关系复杂，在节点规模大，并且其中一些节点具有复杂的边缘关系时可以使用混合方法。
 <div align=center><img width="800" height="500" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/fifth_day_files/fifth_day_notes/5-12.jpg"/></div>
<p align=center size="16">图5-12 混合方法示意图<p>
    
 ### 三、工具与应用
Tulip：信息可视化框架，专门用于分析和可视化关系数据。
Gephi：用于各种图形和网络的领先的可视化和探索软件。
 
