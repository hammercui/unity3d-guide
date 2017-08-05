本文档分为以下部分

* [unity3d下载与安装](#unity3d下载与安装)
*  [IDE的准备工作](IDE的准备工作)
*  [unity3d基础入门](unity3d基础入门)
*  [unity3d进阶](#unity3d进阶)
*  [c#语言](c#语言ß)


## unity3d下载与安装

[unity3官网所有下载地址](https://unity3d.com/cn/get-unity/download/archive)：注意，unity3d个人版与专业版是一个安装文件，区别在于专业版登录时需要license。个人版已经包含了unity3d引擎核心的全部工具，选用这个就行。

[全系列Unity4.x.x到2017.1.0破解Win&Mac!最新Unity2017.1.0p2&4.7.2f1破解](http://www.ceeger.com/forum/read.php?tid=23396):个人感觉专业版破解就是比个人版多了个皮肤，其他功能还是没有，专业版其他功能都需要网络支持。



## IDE的准备工作
c#的ide有以下三种：

*  MonoDevelop，安装自带的跨平台ide。个人感觉不太好用
*  Visual Studio for mac:微软大法好，用过都说吊。但是安装太慢，pass了
*  JetBrans Rider:跨平台c#的ide。jb公司出品，用过AndroidStudio,WebStorm的自然懂，所以就是你了。

### Rider的安装与配置

[jetbrains Rider下载地址](https://www.jetbrains.com/rider/)





## unity3d基础入门
>我们最好是带着问题去学习

### 问题

* 什么是调度器，而不是update自己维护状态？
* 什么是不依赖component，如何做数据驱动？
* level与scene的关系？
* 什么是利用组件的架构，如何减少c#的继承。
* 什么是星型框架+事件机制？
* unity的渲染流程和ShaderLab
* 如果解决单一DLL过大？
>建议游戏无关的底层代码尽量放到Plugins里，能单独做成DLl的一定要提出来打包

* 如何做tag,layer的规划
* 如何用状态机取代携程？
* 为甚程序策划必须检车美术资源，其中隐藏着什么惊天秘密？
* 为什么即便是直接使用系统shader，也要拷贝出来，不能直接引用。
* 有什么好的代码管理方式。
>

 

### 游戏常用的算法

* 相交性检测
* 无缝地图加载
* aoi
* 游戏资源管理，性能分析，游戏架构


## c#语言

从unity2017开始，使用.net Framet3.5 和4.6对应c#语言版本3.0和6.0。

.net版本与c#版本对比图如下：

|.net framework	|c# version|	note|	date
|---|---|----|---|
|.net 3.5	|3.0|	vs2008 |	2007-08|
|.net 4.0	|4.0|	vs2010	|2010-04|
|.net 4.5 |5.0|	vs2012/13	|2012-10
.net 4.6	|6.0|	vs2015|	2015-07

### 必备的知识点

* 事件驱动的编程模型，比如delegate/event ,BeginInvoke

### 进阶知识点

* 图形学
* 图形学基本原理
* OpenGL


## 推荐的书单

* 《Unity Shader入门精要》
* 《游戏编程模式》
* 《游戏人工智能编程精粹》
* 《深入理解C#》
* 《3D游戏编程大师技巧》（上下两册）
* 《3D数学基础：图形与游戏开发》
* 《游戏引擎架构》
* 《游戏开发中的物理学》
* 《Unity 3D人工智能编程》



