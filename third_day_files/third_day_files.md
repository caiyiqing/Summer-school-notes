# 2019浙江大学可视化暑期学校 - 第三天
## 课程：数据释义
#### 讲师简介：浙江工业大学计算机科学与技术学院数字媒体技术专业系主任，副教授，硕导。研究兴趣是大数据分析与可视化。
#### 课程简介：本次课程概要地介绍数据可视化的基本流程和核心步骤，总结基本的可视化图表映射方法，并阐述数据可视化的基本设计概念。

<div align=center><img width="800" height="500" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/third_day_files/third_day_notes/3-1.jpg"/></div>
<p align=center size="16">图3-1课程内容概要<p>
  
#### 今天的课程内容分为三个部分：
<br>可视化过程模型
<br>可视编码原则
<br>视觉分析模型

### 一、可视化过程模型
可视化过程模型分为三种过程模型：
    概念模型
    数据状态引用模型
    可视化引用模型
#### 概念模型
概念模型主要讲的是原始数据经过数据分析、过滤、映射和编码绘制的过程转换为图形式的数据的过程。
<div align=center><img width="800" height="500" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/third_day_files/third_day_notes/3-2.jpg"/></div>
<p align=center size="16">图3-2科学可视化系统的概念模型<p>
  
#### 数据状态参考模型
数据状态参考模型，是从数据的形式来描述可视化的过程的，先从数值转变为可以理解分析的抽象数据类型，然后在进行可视化表示变为视图。

<div align=center><img width="800" height="500" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/third_day_files/third_day_notes/3-3.jpg"/></div>
<p align=center size="16">图3-3数据状态引用模型<p>
 
#### 可视化参考模型
可视化参考模型相较于前两种模型的区别在于，在流程中引入user交互反馈，形成了可视化闭环回路，使得用户可以在可视化的任何阶段进行交互。同时介绍了Java可视化工具包Prefuse。
 
 <div align=center><img width="800" height="500" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/third_day_files/third_day_notes/3-4.jpg"/></div>
<p align=center size="16">图3-4数据状态引用模型<p>
  
 ### 一、可视化编码原则
 #### 可视化参考模型
 可视化编码原则分为：数据类型、视觉编码、颜色三个部分
 #### 数据类型
 数据共有两种数据：有序和无序数据。
 <br>其中**有序数据**包括：
 * 有序的连续数据：如（温度、高度、能定量表示的数值数据）大致有以下两种
    * 区间数据：0的位置不是固定的，如:日期1月19日、位置等
    * 比值数据：0的位置/原点是固定的，如：测量数据(长度、质量)
 * 有序的离散数据：如（周一、周二。小、中、大等）
<br>其中**无序数据**举例：水果类型：苹果、香蕉、橘子；颜色类型：红、蓝、绿；表格中的序号。
<div align=center><img width="800" height="500" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/third_day_files/third_day_notes/3-5.jpg"/></div>
<p align=center size="16">图3-5数据类型<p> 
####课堂举例：
<div align=center><img width="800" height="500" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/third_day_files/third_day_notes/3-6.jpg"/></div>
<p align=center size="16">图3-6数据类型举例<p>
**上图中绿色的序号代表无序数据，红色代表有序连续数据，蓝色代表有序离散数据**
  
### 二、可视编码原则
#### 视觉编码通道和元素
可视编码通道包括：位置、大小、灰度、纹理、颜色、方向、形状
<br>可视编码元素包括：点、线、面、空间
<div align=center><img width="800" height="500" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/third_day_files/third_day_notes/3-7.jpg"/></div>
<p align=center size="16">图3-7视觉编码表<p>
上图纵轴表示视觉通道（位置、大小、灰度）、横轴表示视觉元素（点、线、面）
<br>在可视化中，我们需要先选择合适的mark标记，再选择用哪个视觉通道来控制。
  
#### 颜色信息
 颜色这种视觉通道中，如何表示连续有序数据、离散有序数据和不连续数据的编码
  <div align=center><img width="800" height="500" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/third_day_files/third_day_notes/3-8.jpg"/></div>
<p align=center size="16">图3-8颜色编码表<p>
  
#### 编码有效性
  在进行视觉编码时，视觉通道的选择要和数据类型相匹配，最重要的数据属性要用最有效的视觉通道表示。编码有效性排名如下图
  <div align=center><img width="800" height="500" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/third_day_files/third_day_notes/3-9.jpg"/></div>
<p align=center size="16">图3-9通道:表现力类型和有效性排名<p>
  
### 三、视觉分析模型
主要介绍可视化设计的层次嵌套模型，用来解决What-Why-How的问题。
<br>数据可视化等你设计简化为4个级联的层次：
1. 定义域，找到真实用户需求；
2. 抽象层，将数据映射到抽象且通用的数据类型；
3. 编码层，设计与数据类型相匹配的视觉编码和交互方法；
4. 算法层，使用高效的算法实现系统。
  <div align=center><img width="800" height="500" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/third_day_files/third_day_notes/3-10.jpg"/></div>
<p align=center size="16">图3-10层次嵌套模型<p>

### 四、React框架介绍与应用
React官方介绍：定义用户接年的JavaScript库
<br>**基于Web构建UI**，是当下最流行，也是最便捷的方式.
<br>**构建平台**：浏览器，构建元素：HTML界面、CSS 样式、JAVASCRIPT 交互行为。
<br>**React学习资源：**
* [React官网](https://zh-hans.reactjs.org/)
* [文档](https://zh-hans.reactjs.org/docs/getting-started.html)分特性介绍React的功能
* [教程](https://zh-hans.reactjs.org/tutorial/tutorial.html)
* [API参考](https://zh-hans.reactjs.org/docs/react-api.html)
* API查阅应用：Dash(Apple全平台)，Zeal(Windows)



