# 2019浙江大学可视化暑期学校 - 第十天
## 课程：科学可视化
#### 讲师简介：陶煜波，浙江大学计算机学院副教授，计算机辅助设计与图形学国家重点实验室。研究兴趣是科学可视化与可视分析。
#### 课程简介：科学可视化是一个跨学科与研究应用领域，主要关注的是三维现象的可视化，如建筑学、气象学、医学或生物学方面的各种系统。重点在于对体，面以及光源等等的逼真渲染，还包括某种动态成分。学可视化是许多科学技术工作的一个构成要素。这些工作之中通常会包括对于科学技术数据和模型的解释、操作与处理。科学可视化工作者对数据加以可视化，旨在寻找其中的种种模式、特点、关系以及异常情况。

 <center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/tenth_day_files/tenth_day_notes/10-1.jpg">
</center>
<p align=center size="16">图10-1课程内容概要<p>
  
 #### 二维数据可视化
2D数据主要包括医学数据和地理数据。主要的可视化方法有颜色映射、等值线和高度图三类。等值线的绘制方法为移动四边形法。其基本思想是逐个处理二维空间标量场的网格单元。移动四边形法共16种情况，数值划分为 “大于等于阈值”、“小于阈值”，很容易画出局部等值线。
 <center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/tenth_day_files/tenth_day_notes/10-2.jpg">
</center>
<p align=center size="16">图10-2等值线绘制法则<p>
  
 #### 三维数据可视化
三维数据例如医学断层扫描设备获取的CT三维影像，仿真模拟产生的温度、气压、湿度分布数据。主要的可视化方法为间接体绘制和直接体绘制。
1. **间接绘制方法**：将体数据转换为面数据，通过等值线的方法间接绘制。移动立方体法算法类似于移动四边形法。通过线性插值法得到交点的位置。
 <center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/tenth_day_files/tenth_day_notes/10-3.jpg">
</center>
<p align=center size="16">图10-3三维体素的等值线绘制法则<p>
 
 2.**直接绘制方法**：直接体绘制采用光学贡献积分模型，通过光的吸收和发射，体积渲染积分的数值解决方案，将体素空间的数据转化为像素空间数据，陶老师主要对其中的图像空间扫描法进行了详细讲解。合成公式如下：
<center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/tenth_day_files/tenth_day_notes/10-4.jpg">
</center>
<p align=center size="16">图10-4光学贡献积分模型<p>
其中Ci和Ai分别是在体纹理上采样所得到的颜色值和不透明度。
间接体绘制的优点是能够一次性展示三维标量场的整体信息和内部结构，下图展示了采用间接绘制（左）和间接绘制（右）的方法来重构图像。
<center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/tenth_day_files/tenth_day_notes/10-5.jpg">
</center>
<p align=center size="16">图10-5绘制方法比较<p>
  
#### 向量场和张量场可视化
* **向量场**
向量场数据集由矢量分量及其大小给出，一般显示场的方向信息和传送模式，空间向量场的核心目标是设计感知有效的流表示方式绘制其流动信息。向量场可以提取一些线、面来提取特征。选择合适的区域增加数据点，并避免遮挡的情况。
<center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/tenth_day_files/tenth_day_notes/10-9.jpg">
</center>
<center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/tenth_day_files/tenth_day_notes/10-6.jpg">
</center>
<p align=center size="16">图10-6向量场流体图<p>
向量场数据可视化方法有图标法、几何法、纹理法、拓扑法。
  <center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/tenth_day_files/tenth_day_notes/10-7.jpg">
</center>
<p align=center size="16">图10-7图标展示方法<p>
 <center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/tenth_day_files/tenth_day_notes/10-8.jpg">
</center>
<p align=center size="16">图10-8通过几何的方法展示<p>
                                           
* **张量场**
张量场的数学理论是数学界的研究热点，逐步在图形和可视化领域得到应用。将数据组织为张量可为分析三维空间数据提供有效的工具。

#### 科学可视化工具包
[VTK](http://www.vtk.org/) (Visualization Toolkit)：提供了最先进的3D渲染技术。
Voreen (volume rendering engine)：用于交互式可视化和可视分析多模态体数据集。
