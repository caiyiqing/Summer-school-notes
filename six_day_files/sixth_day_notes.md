# 2019浙江大学可视化暑期学校 - 第六天
## 课程：文本与文档可视化
#### 讲师简介：傅四维，之江实验室副研究员，博士毕业于香港科技大学。研究兴趣为文本可视化，人工智能辅助可视分析。
#### 课程简介：文本信息无处不在，譬如，邮件、新闻、工作报告等等都是日常处理的信息。面对文本信息的爆炸式增长和日益加快的工作节奏，通过人工阅读大量文字来获取信息暗藏着的信息理解速度滞后的问题。利用可视化增强人类对文本和文档的理解正是在这样的背景下应运而生。文本可视化应用范围广泛；便签云技术已是诸多网站展示其关键词的常用技术；信息文本图是美国纽约时报等各大纸媒辅助用户理解新闻内容等必备方法。文本可视化还与其他领域结合，如信息检索技术，可视地表达信息检索过程、传达信息检索结果。

<div align=center><img width="500" height="300" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/six_day_files/six_day_notes/6-1.jpg"/></div>
<p align=center size="16">图6-1课程内容概要<p>

### 一、文本可视化
#### 文本分析技术
傅四维老师讲了文本可视化的核心技术点。
* **Tokenization**:主要用于提取出文本中的关键字，先提取出文本的单词（文本预处理：分词、统计词频、去掉无用的词（“stop words“：a、the、that、etc）、去掉标点符号/链接等。

* **文本主题向量化**：Word2vec、Doc2vec以及fastText。Word2vec技术是用神经网络的方法，将一个维度很高的（取决于词窗口的大小）高维空间嵌入到维数低得多的连续向量空间中，每个单词或词组映射成一个上下文有关的vector，上下文有关体现在语义相关的不同词的向量距离靠的会很近。而Doc2vec与Word2vec相比，对所有的词整体进行向量化（如简单的求平均或其他更复杂的方法），用于比较不同文档之间的相似性。

* **文本主题提取**：对大量文档进行主题分析，如在同一个文档中，可能存在不同的主题：T1、T2…,而在同一个Topic中，有会有很多相关的词汇如W1、W2…且对应的主题或关键词它们都可以有一个概率值。现在主流的技术有Latent semantic Indexing、pLsl、LDA等。主题提取的作用可以用来挖掘文本中topic的层次关系、时间变化等。

#### 文本可视化技术
**文本分析关键技术**
* **词云Wordle**
1. 有一个文本：先提取出文本的单词（文本预处理：分词、统计词频、去掉无用的词、去掉标点符号/链接、layout（展示）：对词频进行排序，词频最多的最大放中间，第二大的词先放中间然后进行冲突检测，检测是否有重叠的部分，重叠之后将单词以某个距离和角度向外扩，第三词也是从中间开始，冲突检测再随机往外扩） 常见的：四叉树（quad-tree）。
2.可视化：可对词的位置做限制：同一个词在不同词云中距离差距不能太大、同一个词的相对关系不变在传统的wordles里增加可编辑的功能（拖动、自动对齐、编辑、调整颜色等功能）
<div align=center><img width="500" height="300" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/six_day_files/six_day_notes/6-2.jpg"/></div>
<p align=center size="16">图6-2Wordle可视化展示<p>

* **文档卡片**
<br>在文档中总结包含关键字和图像的文档卡片式空间中的布局
 <div align=center><img width="500" height="300" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/six_day_files/six_day_notes/6-3.jpg"/></div>
<p align=center size="16">图6-3文档卡片可视化展示<p>

* 可变形词云可视化
<br>适用于时间/序数文件数据，可做成可变形词云，可视化对象必须随着时间有明显变化
 <div align=center><img width="500" height="300" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/six_day_files/six_day_notes/6-4.jpg"/></div>
<p align=center size="16">图6-4随时间可变形词云可视化<p>

* 时序性文本内容可视化
 <div align=center><img width="500" height="300" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/six_day_files/six_day_notes/6-5.jpg"/></div>
<p align=center size="16">图6-5随时间社交媒体可视化<p>
  
* 特征分布可视化
 <div align=center><img width="500" height="300" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/six_day_files/six_day_notes/6-6.jpg"/></div>
 <div align=center><img width="500" height="300" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/six_day_files/six_day_notes/6-7.jpg"/></div>
  <p align=center size="16">图6-6特征分布可视化举例<p>
    
* 情绪分析可视化
<br>意见和情绪分析，判断文本的赞美或批评、积极消极情绪。
 <div align=center><img width="500" height="300" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/six_day_files/six_day_notes/6-8.jpg"/></div>
  <p align=center size="16">图6-7特征分布可视化举例<p>
  
* 信息查询可视化
<br>通过可视化引导搜索/查询信息，如了解搜索结果、发现信息中的分布模式、查询本身或搜索结果的相似性
 <div align=center><img width="500" height="300" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/six_day_files/six_day_notes/6-9.jpg"/></div>
  <p align=center size="16">图6-8信息查询可视化举例TileBar<p>
  
* 软件可视化
<br>源代码可以视为特殊类型的文本，软件可视化级别分为源文件、功能/模块的结构，以及它们之间的关系。
 <div align=center><img width="500" height="300" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/six_day_files/six_day_notes/6-10.jpg"/></div>
  <p align=center size="16">图6-9软件可视化举例<p>
 
### 二、多媒体可视化
 <div align=center><img width="500" height="300" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/six_day_files/six_day_notes/6-11.jpg"/></div>
   <div align=center><img width="500" height="300" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/six_day_files/six_day_notes/6-12.jpg"/></div>
   <div align=center><img width="500" height="300" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/six_day_files/six_day_notes/6-13.jpg"/></div>
  <p align=center size="16">图6-11对媒体可视化举例<p>
