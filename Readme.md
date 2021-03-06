# LipstickTest口红试色项目

对人脸嘴唇区域进行模拟口红试色。

#### 目前实现情况【200426】

根据dlib的人脸关键点，提取出68个关键点，然后嘴唇区域作为凸包；

再判断点是否在嘴唇区域（外嘴唇凸包以内，内嘴唇凸包以外之间区域定义为嘴唇区域），

根据输入的口红hsv值进行嘴唇凸包区域染色。

添加了UI选择H、S界面。

进行了边缘自然化处理，根据出现最多的像素点进行边缘细节处理，将外嘴唇区域细分为左右两个凸包（ok(cy-4-23).py）。

#### 项目陈述：

本科期间的创新创业项目，项目动机是个人对口红的狂热购买欲（尽管做着做着就不那么的热爱了）。最早是想用android做app，但是调试实在是太麻烦，提取关键点后的图像处理总是炸内存。

这几天临近结项，因为我本科毕设一直写python就看了下python的图像处理，发现还挺easy，就写了下，可以基本实现主要功能。

#### 技术路线：

python环境下opencv+dlib人脸识别

#### 环境配置：

anaconda新建一个python环境，激活环境后：

pip install cmake

pip install boost

（电脑还要确保配置了VS 2017环境）

pip install dlib

#### 当前效果展示图：

从光妹变超A光姐！

<img src="https://github.com/zhxjz/LipstickTest/raw/master/resultShow/1.jpg" height="300"/>

我光妹就是涂死亡色号都好看的自带光环小天使！

<img src="https://github.com/zhxjz/LipstickTest/raw/master/resultShow/2.jpg" height="300"/>

简单UI界面：

<img src="https://github.com/zhxjz/LipstickTest/raw/master/resultShow/UI.gif" height="600"/>

#### 后续组员完善的尝试方向（4.12-4.23时段每天晚上十点check）：

1. 口红颜色的调整，多几种配色的选择。（hpf）
   14号配置，16号开始每两天汇报进度。

2. ~~rgb转换为hsv空间，尝试调整达到口红效果。内外凸包分离。（hsc）~~
   ~~14号配置，16号开始每两天汇报进度。~~

3. ~~UI添加选择颜色亮度对比度。（wxd）~~
   ~~14号配置，16号开始每两天汇报进度。~~

4. ~~边缘自然化处理。（cy）~~
   ~~14号配置，16号开始每两天汇报进度。~~

