# 2019浙江大学可视化暑期学校 - 第四天
## 课程：可视化设计、变换与编码
#### 讲师简介：石洋，同济大学设计创意学院智能大数据可视化实验室助理研究员，主要研究方向是人机交互及大数据可视化。
#### 课程简介：本次课程主要介绍了成型的交互模式、技术和理念，，阐述了它们各自的优缺点以及相应的应用场景。同时也介绍了当前被广泛应用的两种范式，即概览+细节和焦点+上下文。

<div align=center><img width="800" height="500" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/fourth_day_files/fourth_day_notes/4-1.jpg"/></div>
<p align=center size="16">图4-1课程内容概要<p>
  
### 一、交互类型
#### 信息可视化。
信息可视化有两个主要的组成部分:用户关注的对象表示、用户可以操作的交互。

<div align=center><img width="800" height="500" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/fourth_day_files/fourth_day_notes/4-2.jpg"/></div>
<p align=center size="16">图4-2信息可视化交互<p>
  
#### 七种交互方式
1. **选择**
<br>选择的实现主要包括弹出信息标签和鼠标选择两种。弹出信息标签表示：悬停鼠标光标会显示项目的详细信息。弹出的标签必须遵循可读性、指引性和相互不遮挡三大标准。但当数据量较大或数据结构比较复杂时，会造成严重的视觉混乱，很难实现精准的选择操作。

下图所示，在地图上选择一个区域并使用放大技术来可视化选择的区域
<div align=center><img width="800" height="500" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/fourth_day_files/fourth_day_notes/4-3.jpg"/></div>
<p align=center size="16">图4-3选择交互方式举例<p>
  
2. **探索**
<br>允许用户能够关注不同的数据子集并探索，可以通过平移、缩放、对象之间的跳转等来实现该目的，有效克服了显示尺寸的限制。

3. **重配**
<br>重配即重新布局，即通过改变数据元素在空间中的排列来帮助用户来观察和探索数据。比如改变表的行列顺序、重新排序、重新放置等。

4. **编码**
<br>视觉编码是可视化的核心要素之一，可以通过改变颜色编码、大小、方向、形状等帮助用户找到数据模式。
<div align=center><img width="800" height="500" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/fourth_day_files/fourth_day_notes/4-4.jpg"/></div>
<p align=center size="16">图4-4不同可视编码选择举例<p>

5. **具体化和抽象化**
<br>用户通过交互能够使视图展示更多或更少的数据细节，例如展开子类别、树图、旭日图、几何缩放等。

6. **过滤**
<br>通过设置限制条件、直方图刷取、动态查询等过滤方式，支持用户对数据进行筛选，只显示某些符合条件的数据子集。这种交互方式更加自然，但也存在一些约束。比如必须知道选择条件是什么，同时在面对海量数据时，需要提高计算效率。

7. **关联**
关联主要为通过高亮显示数据对象及其之间的联系，显示与指定项目相关的隐藏数据项。

### 二、交互思想模式
1. **概览+细节**
<br>由于屏幕尺寸的限制，使得数据不能得到充分显示，所以在用户兴趣点发生变化时，需要对视图进行改变。可以通过滚动概览、缩放等展示某一层次的具体细节。通过允许用户移动到不同区域来提供更大的虚拟屏幕

2. **焦点+上下文**
<br>焦点+上下文致力于显示用户兴趣焦点部分的细节，同时提现焦点和周边的关系关联，最简单的比如MAC电脑下的导航图标。
<div align=center><img width="800" height="200" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/fourth_day_files/fourth_day_notes/4-5.jpg"/></div>
<p align=center size="16">图4-5mac桌面导航  <p>
  
### 三、动画
<br>由于用户关注的数据是有限的，当视图进行切换时，如何防止用户关注的东西视觉丢失是一个亟待解决的问题。

### 四、交互与硬件设备
Muti-touch将多点触摸和可视分析相结合，主要用来展示项目。Microsoft Kinect使用大屏和智能手表来帮助用户进行游戏娱乐。其他的一些作品还有Microsoft HoloLens、Makey makey等。

### 可视分析系统搭建的流程
1. **确定需求**
* 面向特定人群的可视系统（使用者访谈）{1 领域知识、2 数据类型、3 目标、4 场景}
* 通用型可视分析系统（需求分析、调研）{数据、任务}
2. **数据流程**
<br>原始数据（多源异构）-数据处理（筛选、清晰、降维/聚类/筛选/清洗/异常检测）-可视化
3. **框架选择**
<br>系统框架：网页前端或者客户端
<br>react vue angular sigmajs（渲染效率高）
<br>可视化框架：考虑其：学习曲线、功能易用性、可视化效率
4. **一般结构**
<br>包括：控制面板、概览视图、细节视图、辅助视图、编码面板
5. **交互模式**
<br>选择、探索、布局、可视化编码、抽象/具体、过滤、链接

