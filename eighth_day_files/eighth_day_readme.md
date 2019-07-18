# 2019浙江大学可视化暑期学校 - 第八天
## 课程：空间与地理数据可视化
#### 讲师简介：巫英才，浙江大学百人计划研究员、博士生导师，入选国家青年千人计划。近期聚焦于城市大数据、体育大数据和社交媒体大数据的可视分析研究。
#### 课程简介：主要介绍了地理数据的可视化方法和常用的地理信息数据集，此外还介绍了城市大数据的可视化方法。

<center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/eighth_day_files/eight_day_notes/8-1.jpg">
</center>
<p align=center size="16">图8-1课程内容概要<p>

### 一、地理数据可视化
#### 地理数据
对象的位置信息由地理数据或基于位置的数据来描述，地理空间是人类生活的空间，这使得信息载体和绘图非常特殊和有价值。
地理数据产生途径：手机、智能手表、gps传感器
手机上基于位置的信息：Wechat、谷歌地图、Yelp、Facebook
**如何重现？最基本的载体是地图**

#### 地图投影
地图投影分为等角度投影、等面积投影和等距离投影。不同的投影方式会导致地图不同的形变。
* 等角度投影：会造成投影面积变化。靠近赤道面积小，越往两极面积越大。**地图面积形变严重，数据分析时会产生误导**
* 等面积投影，即投影前后面积大小不变。缺点是会产生比较严重的形变。**牺牲投影的形状来保障面积**
* 等距离投影：即投影前后点与点之间的距离保持不变。适合航线标记

#### 点数据可视化
点数据可视化即将分散在地理空间中包含经位置信息的点，可视化地展示在地图上，常见的方法是直接在地图上重现出来。用点的大小、颜色、形状来编码信息，将每个坐标点直接放置在空间上下文之中，可以利用热力图避免视觉混淆。下图使用点数据可视化展示了世界各国的人们使用社交媒体的不同模式，**将每个国家的位置属性直接在地图上标出，并通过颜色、柱状图、大小来编码属性**
<center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/eighth_day_files/eight_day_notes/8-2.jpg">
</center>
<p align=center size="16">图8-2社交媒体可视化<p>

**可以利用热力图解决可视化大量数据点时造成的视觉混淆问题**。下图是英国交通事故在地图上显示的可视化结果，每个小灯代表一起事故，越亮的地方代表事故频发区。
<center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/eighth_day_files/eight_day_notes/8-3.jpg">
</center>
<p align=center size="16">图8-3交通事故分布图<p>
  
#### 线数据可视化据
对于大量的线数据，视觉复杂度的问题非常严重。针对不同的应用需求，应选择合适的解决方法。如果可视化的目的是理解数据整体模式，而不是展现每一条线段，可通过合适的渲染方法，合理地视觉融合大量的线条，让数据内在的模式变成容易观察到的视觉元素。
线数据包括：起点、终点和中间所有位置。**适合道路网络上的可视化（用颜色编码该道路的交通状况）用离散的坐标点构造轨迹，并利用基于线段的可视化方法加以呈现**
有意思的可视化方法：Flow Map（算法：聚类、展示线）
<center>
    <img src="https://https://github.com/caiyiqing/Summer-school-notes/blob/master/eighth_day_files/eight_day_notes/8-4.jpg">
</center>
<p align=center size="16">图8-4飞行轨迹可视化<p>

**线段的空间数据可视化**
<br>**对于大规模的轨迹数据，边捆绑技术和核密度估计可以很好地解决视觉混淆的问题**。通过层次聚类计算连线绑定，根据所连接地点之间的位置关系进行自下而上的层次聚类，得到一个包含所有需要连接的地点的层次结构。
<center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/eighth_day_files/eight_day_notes/8-5.jpg">
</center>
<p align=center size="16">图8-5基于线段的空间可视化<p>

#### 区域数据可视化
在区域数据可视化中常用的技术包括Choropleth地图、Cartogram等。
<br>分级统计图Choropleth 。在整个制图区域的若干个小的区划单元内（行政区划或者其他区划单位），根据各分区资料的数量（相对）指标进行分级，并用相应色级或不同疏密的晕线，反映各区现象的集中程度或发展水平的分布差别。下图为2016年美国总统大选结果。民主党候选人希拉里和共和党候选人川普胜出的州分别用蓝色和红色表示。
<center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/eighth_day_files/eight_day_notes/8-6.jpg">
</center>
<p align=center size="16">图8-6Choropleth地图示例<p>
Choropleth地图的可视化方法，忽略了细节的数据属性，如上图中没有考虑人口分布。它没有考虑到红色国家的人口平均显着低于蓝色国家的人口。 蓝色可能面积很小，但它们代表了大量选民，当数据在显示空间较小的地方累积时，会出现不匹配，反之亦然。这种不匹配很可能会误导观众。
<br>比较统计图（cartogram）来修正地图：地图上的每个州根据人口做缩放，某些州根据人口数量被放大缩小，而地理位置关系还基本保持不变。在这张地图上，我们可以清楚地看到蓝色的区域大大超过红色
<center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/eighth_day_files/eight_day_notes/8-7.jpg">
</center>
<p align=center size="16">图8-7cartogram修正的地图<p>


#### 地理数据集
OpenStreetMap 可以直接下载城市路网数据

<br>如果需要将自己的数据在地图上展示，可以使用以下：
* Google/Baidu API
* 开源城市路网数据[OpenStreetMap](http://www.openstreetmap.org)
* 香港政府公开数据[HK government dataset](http://data.gov.hk)
* 纽约市公开数据[NYC Open Data](https://opendata.cityofnewyork.us)
* 美国政府公开数据[Data.gov](https://www.data.gov)


### 二、城市数据可视化
基于城市大数据，利用信息技术精准 地分析以及高效地解决城市的问题
<br>**关键问题**：
* 如何从大规模复杂的城市数据集中得出结论
* 如何利用专家的领域知识发现新的见解
* 如何传递并解释从数据中得到的见解
<br>**三个目标**：
* 多层次的可视化（首先展示整体概述，可以缩放和过滤等交互，然后按需要展示细节）
* 支持混合引导探索的富交互行为
* 叙述性地总结数据中挖掘得到的见解
#### 时间数据可视化
<center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/eighth_day_files/eight_day_notes/8-8.jpg">
</center>
<p align=center size="16">图8-8时间数据可视化形式<p>
  
#### 空间数据可视化
<center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/eighth_day_files/eight_day_notes/8-9.jpg">
</center>
<p align=center size="16">图8-9基于点、线、面的空间数据可视化形式<p>
  
#### 时空数据可视化
<center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/eighth_day_files/eight_day_notes/8-10.jpg">
</center>
<p align=center size="16">图8-10时空属性的可视化方法<p>
 
#### 城市数据集
* [美国政府公开数据](https://www.data.gov)
* [中国政府公开信息数据集](http://govinfo.nlc.cn/)
* [中国国家数据National Data](http://data.stats.gov.cn/)
* [中国气象数据网](data.cma.cn)
* [上海市政府数据服务](http://data.sh.gov.cn/)

#### 如何清洗数据
获取数据之后需要对数据进行清洗才能使用，数据清洗可以使用Google Refine和Trifacta等软件。在有了加工之后的数据后可以通过Tableau、Power BI、D3等方法对其进行可视化呈现。
**[Google Refine](https://mashable.com/category/google-refine/)（强烈建议学习）**，做大数据分析时，百分之50以上的时间花在大数据清理上。
Trifacta （牺牲灵活性 操作稍微简单）、基于D3的地理可视化库DATAMAP。

#### 城市大数据案例分析
老师通过基于大数据的广告牌位置选取问题和基于道路放大技术的交通流量分析等城市数据可视化实例为我们介绍了在城市数据可视化中用到的一些方法。
1. 基于大数据的广告牌位置选取问题
影响广告牌放置地点的因素:交通流量、车流速度、轨迹OD（目标人群住和工作的地方）、周边环境。
**关键挑战**：
* 如何以较小的代价获得详细的数据（使用出租车轨迹、人群轨迹和统计数据）
* 如何快速生成一个好的广告牌放置方案（计算能力+领域知识）通过人机协同的方式
* 如何可视化地比较多个放置方案并确定最优的一个
**数据集**：
基于天津数据集的案例分析、路网数据：133,726条道路片段，99,007个顶点、GPS轨迹数据：400万条出租车轨迹、POI数据：15万个坐标

<center>
    <img src="https://github.com/caiyiqing/Summer-school-notes/blob/master/eighth_day_files/eight_day_notes/8-11.jpg">
</center>
<p align=center size="16">图8-11广告牌投放可视分析系统<p>
因此提出了一个系统，它结合了先进的数据挖掘方法和交互式可视化技术，首先预处理原始数据，构建四个索引，然后使用这些索引提取有用信息。然后有一个位置优化器，旨在通过使用数据挖掘方法推荐位置。 解决方案生成器可以与位置优化器交互，以帮助用户以交互方式改进解决方案。最后，解决方案资源管理器旨在促进多个解决方案之间的可视化探索和比较。
