# 2019浙江大学可视化暑期学校 - 第九天
## 课程：高维数据可视化
#### 讲师简介：曹楠，同济大学教授。主要研究方向是大数据分析及可视化，研究成果涵盖了数据可视化、数据挖掘、机器学习、及人机交互多个技术层面。
#### 课程简介：高维数据泛指高维和多变量数据，高维指多个相互独立的维度，而多变量指相互潜在关联的多个变量。这里介绍高维数据可视化方法，不区分这两种差异，统一采用属性代表独立空间的维度和多维度数据中的变量。本次课程将从数据变换，数据呈现和数据交互三个角度介绍高维数据可视化方法。

<center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/ninth_day_files/ninth_day_notes/9-1.jpg">
</center>
<p align=center size="16">图9-1 课程内容概要<p>
  
 ### 高维数据可视化
**数据维度**
<br>数据包括1D、2D、3D、高维度数据，每个数据属性看做一个维度、通过维度可以分析数据之间的关联，不同的数据属性具有不同的数据类型
**在数据分析时主要是针对数值类型的属性进行计算和展示**

**高维数据可视化方法**
* **正交坐标系**
<br>正交坐标系；优点：简单直观、最容易去读。缺点：轴特别占空间、效率低。
<br>因此在正交坐标系基础上改进引入：Scatter-plot Matrix，可以放入不同维度的坐标系。对每个维度对应的2-D图。显示不同维度之间的相关性。二维图数量与维度平方成比例。**任意2个轴变成一个坐标系，用散点图矩阵表示**
<center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/ninth_day_files/ninth_day_notes/9-2.jpg">
</center>
<p align=center size="16">图9-2 Scatter-plot Matrix坐标系<p>
  
 * **平行坐标系**（应用广泛）
平行坐标系于1985年提出，用于多维数据。坐标轴是竖着的平行轴，多个坐标轴表示多个维度的属性，轴上的交点表示相应属性的值。
优点：可以展现更多的维度,缺点：线多了之后，相互交错难以追踪，不适合展示非常大规模的数据。使用平行坐标轴必须要交互，点击每个轴之间的区域，产生交互细节，高亮出其中某条数据。**平行坐标系中有效的聚类不超过5个**
<center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/ninth_day_files/ninth_day_notes/9-3.jpg">
</center>
<p align=center size="16">图9-3 平行坐标系<p>

**如何减少平行坐标的混乱**?
原则：不能修改数据
* 过滤:根据数据密度进行过滤，高亮显示密度高的区域。
* 聚类:不显示每个数据的细节，显示数据整体的信息。
* 采样：下采样百分之50的数据，数据丢失。可做成放大镜（**不推荐**）
* 可视化层面的聚类：将直线聚类成曲线、捆绑在一起。做成Flow的形式
* 排序：对维度进行排序，将相似度高的维度放在一起（重要）（Ferdosi&Roerdink）
* 增强：改变某些线的透明度，高亮高密度数据，密度低的时候看不清。
<center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/ninth_day_files/ninth_day_notes/9-4.jpg">
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/ninth_day_files/ninth_day_notes/9-5.jpg">
</center>
<p align=center size="16">图9-5 平行坐标系<p>

**降维:从高维投影到低维** 
数据降维就是用线性或非线性的方法将高维数据投影到低维空间的同时尽可能的保证信息不损失或尽可能小的损失。曹楠教授主要介绍了两种线性的降维方法，PCA和MDS。
1. PCA方法：一般是从高维投影到二维：找到一个投影面，将数据均匀分开，若降维到2维，**需要计算自己损失了多少信息量**。
2. MDS方法：在低维空间中保持高维空间的距离。举例：文档数据。每个点代表一个文档。一个文档有1W个高频词，投影到2维平面，若文档包含的词接近的话，投影的距离就比较近。
<br>降维算法过程略。

**小图标表示方法Glyph-based Method**
在可视化视图中加入小图标元素，展现更多的细节数据维度。如下，星形图是基于象形编码方法的一个很好的例子，它将不同维度的值体现在星形角的长度，直观的体现数据的不同维度的特性。
<center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/ninth_day_files/ninth_day_notes/9-6.jpg">
</center>
<p align=center size="16">图9-6 小图标表示法<p>
小图标表示法的设计方式有如下，这些图标可以带来丰富的数据维度
<center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/ninth_day_files/ninth_day_notes/9-7.jpg">
</center>
<p align=center size="16">图9-7 小图标的设计风格<p>

**基于像素的表示方法**
基于像素的方法由于屏幕的分辨率比较有限，目前极少使用，因此不作介绍。


**Small Multiples的方法**
将数据用一些小的类似的图都画出来进行比较，使用多视图来展示高维数据，在多个视图中设置交互，使视图的排版风格可以改变
<center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/ninth_day_files/ninth_day_notes/9-8.jpg">
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/ninth_day_files/ninth_day_notes/9-9.jpg">
</center>
<p align=center size="16">图9-9 Small Multiples的方法<p>

**视觉诊断**
可视化诊断**提出一组视图本身展现结果的评估方式**，评估轨迹、形状、分布、是否包含数据的异常情况。**可以用计算机来衡量你的可视化效果是否优良**，也可以在多个视图中**让机器帮你选择更好的（感兴趣的可视化模式）视图**。

下图是Scagnostics (Scatter plots + Diagnostics)的示意图，即用一系列方法将各个scatter plot视图根据不同的类型的可视化（如趋势、形状、密度等）的效果进行排序，如在trend列排序越高，则代表这个图对趋势的体现效果很好。
<center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/ninth_day_files/ninth_day_notes/9-10.jpg">
</center>
<p align=center size="16">图9-10 视觉诊断示意<p>

#### 总结
* 第一大类(多维散点正交坐标系、平行坐标系、数据降维)是最有用的。
* 数据评估在数据量很大的时候帮助我们快速找到最有用的视图。
* Glyph的方法可以个性化的定制视图。
* Small multiples适用于用同一种可视化比较不同属性的变换。




