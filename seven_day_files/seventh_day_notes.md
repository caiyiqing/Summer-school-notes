# 2019浙江大学可视化暑期学校 - 第七天
## 课程：时间数据可视化
#### 讲师简介：吴向阳，杭州电子科技大学计算机学院副教授，硕导。研究兴趣是数据可视化与可视分析。
#### 课程简介：时间是一个非常重要的维度和属性，随时间变化、带有时间属性的数据称为时变数据。处理时变数据的方法有时候与顺序型有相似之处，时空数据指的是包含时间变量和空间位置的数据，相当于在空间数据上增加了时间维度

<div align=center><img width="800" height="500" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/seven_day_files/seven_day_notes/7-1.jpg"/></div>
<p align=center size="16">图7-1课程内容概要<p>
  
### 一、时间数据可视化
#### 时间数据设计空间
时间数据无处不在，包括：股价、人的血压、中国年降雨量、网页点击、微信消息等。时间数据可以分为时间时间序列数据和时变数据。时间数据的可视化设计空间涉及三个维度，即表达、比例尺和布局。
* 表达：将时间轴映射到二维平面的表达形式（直线、元、表格、螺旋、任意曲线）
* 比例尺：时间轴的尺度（按时间顺序均匀的时间轴、相对时间轴、对数时间轴等）
* 布局：线性和多视图、流数据形式、树图形式
<br>通过组合三个维度上的不同方法，就可以得到不同的时间数据可视化结果。
<center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/seven_day_files/seven_day_notes/7-14.jpg">
</center>
<p align=center size="16">图7-2时间数据的可视化设计空间<p>

#### 不同表达布局方式展示
**线性时间投影**
<br>老师首先列举了一些线性时间映射的实例，通过线性映射方式展示将时间数据显示为2D线图，X轴为时间，Y轴为另一个变量
<center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/seven_day_files/seven_day_notes/7-2.jpg">
</center>
<p align=center size="16">图7-3线性时间映射方式<p>
  
  **圆形布局投影**
 <br>北京大学通过环形图展示了北京的交通轨迹，将时间维度延螺旋分布，据此研究城市的热点区域和市民的出行模式
 <center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/seven_day_files/seven_day_notes/7-3.jpg">
</center>
<p align=center size="16">图7-4北京交通可视化<p>
  
 **网格布局投影**
  <br>每行表示年份，12个区域表示月份，每小格代表天，非常适合编码每天变化的数据
   <center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/seven_day_files/seven_day_notes/7-4.jpg">
</center>
<p align=center size="16">图7-5网格布局可视化<p>
  
**螺旋布局投影**
  <figure class="half">
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/seven_day_files/seven_day_notes/7-5.jpg">
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/seven_day_files/seven_day_notes/7-6.jpg">
</figure>
<p align=center size="16">图7-6螺旋布局可视化<p>
  
 #### 时间轴尺度选择
 * **对数时间轴**
 <br>、对数时间：为了**凸显比较近的时间事件**，远时间的事件被简单展示。顺序时间轴已经非常了解，这里主要展示对数时间轴，
<center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/seven_day_files/seven_day_notes/7-7.jpg">
</center>
<p align=center size="16">图7-7对数尺度时间轴<p>
  
 #### 多变量时间数据可视化
多变量时变型数据是实际应用中常用的数据集，由于存在多个变量，可视化需要兼顾数据本身属性和数据集的顺序性，以此来展示和挖掘顺序性数据的规律。如下图中每行代表一个变量，用不同的颜色代表不同的属性，可以通过鼠标交互的方式，选择不同的变量，高亮出某个变量的属性，便于观察分析。
<center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/seven_day_files/seven_day_notes/7-8.jpg">
</center>
<p align=center size="16">图7-8多变量可视化展示例_1<p>
下图例2记录了学生在每周见面的数据，可以清楚的分析学生每天的活动规律，该方法将动态网络图的演变状态进行展示，没有列举每一个时间的状态网络图让人们自己去寻找发现规律，可以帮助人们了解动态网络图形的演变趋势。
 <center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/seven_day_files/seven_day_notes/7-9.jpg">
</center>
<p align=center size="16">图7-9多变量可视化展示例_2<p>
 
 ### 二、流数据
 **流数据展示是目前使用最广泛，多用于文本数据：新闻报道事件、舆情分析等**。
 <br>流数据的主要属性为（1）数据可能是无限的。（2）无法知道数据的到达时间和顺序（3）实时处理（4）存在数据错误和数据丢失
<center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/seven_day_files/seven_day_notes/7-10.jpg">
</center>
<p align=center size="16">图7-10流数据可视化示例_1<p>
<center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/seven_day_files/seven_day_notes/7-11.jpg">
</center>
<p align=center size="16">图7-11流数据可视化示例_2<p>
  
 #### 数据离散处理方法
老师详细讲解了符号累计近似（SAX），该方法将时序数据离散化，然后将离散的值分区间用字母表进行对应，就可以把一段原始数据转化为一个字符串，我们可以之后就可以利用字符串的一些算法来对时序数据进行比较，从很大程度上提高了数据计算的时间和空间复杂性。
<center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/seven_day_files/seven_day_notes/7-12.jpg">
</center>
<p align=center size="16">图7-12 SAX示例_2<p>
<center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/seven_day_files/seven_day_notes/7-13.jpg">
</center>
<p align=center size="16">图7-13 流数据可视化工具LogTool<p>  
 
 
### 三、设计原则
* 尽可能显示熟悉的视觉表示
* 提供小型多视图的并排比较
* 空间位置是最强的视觉提示
* 通过显式链接进行协调时，多个视图更有效
* 遵循Shneiderman的口头禅
  * 首先概述，缩放和过滤，然后按照需要增加细节
* 避免突然的视觉变化
* 用户的交互操作应立即获得视觉反馈
* 同时显示多个细节级别可在上下文中提供有用的高信息密度
  
 
