# 2019浙江大学可视化暑期学校 - 第二天
## 课程：视觉与感知
#### 讲师简介：浙江工业大学计算机科学与技术学院副教授。在可视化领域相关期刊和会议发表论文20余篇，曾获浙江省科技进步一等奖。
#### 课程简介：本次课程介绍了可视化中视觉感知和认知的基本概念、可视化中图形形状的应用，此外还介绍了颜色的基本原理以及用于选色的一些工具。

<div align=center><img width="800" height="500" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/second_day_file/second_day_notes/2-1.jpg"/></div>
<p align=center size="16">图2-1课程内容概要<p>
  
### 一、视觉感知
#### 视觉感知和认知的定义。
<br>感知是人们为了理解和表现环境，对于感官信息的组织、识别和解释。
<br>认知是一组包括了关注、记忆、培养和理解语言、解决问题和做出决定的心理过程。认知举例：
* 当人们专注于计数传球次数时，大部分人都会忽略在球员中走过去的大猩猩。该现象表明：记忆在人类认知中扮演着重要的角色，但是有效的记忆是非常有限的。而可视化可以作为一个额外的辅助工具来帮助人们增强这种有效记忆。
* 将两张相似度极高的图片以极短的时间间隔交替播放，人们很难观察出两张照片的相异处。该现象表明：为了观察对象某处的变化，必须将注意力集中在这一点。将这些变化在可视化中变得更突出显眼可以减轻认知压力。
此外，孙老师还介绍了视觉的恒常性原理和颜色的相对性原理。
**要看到对象的变化，必须注意它，使变化可视化，以减少认知负荷**

#### 视觉感知的性质
* 恒常性：形状恒常性、大小恒常性、亮度恒常性、方向恒常性、距离恒常性、位置恒常性
<div align=center><img width="800" height="500" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/second_day_file/second_day_notes/2-2.jpg"/></div>
<p align=center size="16">图2-2视觉感知的恒常性<p>
  
* 相对性&绝对性：感知系统基于相对判断，而非绝对判断
放2-3 2-4 2-5
<div align=center><img width="500" height="300" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/second_day_file/second_day_notes/2-3.jpg"/></div>
<div align=center><img width="500" height="300" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/second_day_file/second_day_notes/2-5.jpg"/></div>
### 二、认知
**人们的已有经验和知识会影响到之后的认知过程**
视觉来源于输入，“当你观察某个事物时，你观察到的东西取决于它本来是什么。但你认为它是什么则取决于你对它的了解程度”。
<div align=center><img width="800" height="500" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/second_day_file/second_day_notes/2-6.jpg"/></div>
<p align=center size="16">图2-6不同的视觉认知<p>

### 三、形状
可视化设计中，我们可以遵循格式塔原则，使用合适的形状可以有效地展现事物特征。
**<br>结构比元素重要，视觉形象首先作为统一的整体被认知**
格式塔原则：
* 接近性、相似性、连续性、闭合性、简单性
* 共势原则、好图原则、对称原则、经验原则

### 四、颜色
目前人们广泛使用的三种颜色系统，以及它们之间的应用场景。电脑：RGB，打印机：CMYK

<div align=center><img width="800" height="500" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/second_day_file/second_day_notes/2-7.jpg"/></div>
<p align=center size="16">图2-7不同的颜色系统<p>

### 五、着色工具
主流选择颜色的工具，有ColorBrewer, Color Farm, Colorgorical, I want hue, Color Hunt, Ambinace, Color Wheel等。

<div align=center><img width="800" height="500" src="https://github.com/caiyiqing/Summer-school-notes/blob/master/second_day_file/second_day_notes/2-8.jpg"/></div>
<p align=center size="16">图2-8ColorBrewer系统<p>

**ColorBrewer适合于颜色编码少于12类的情况，当超过时候可考虑使用形状、纹理、大小来区分**

### 六、可视化编程库
讲解了可视化编程库D3的基础入门和进阶技巧

