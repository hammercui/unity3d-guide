本文档分为以下部分

*  [1.unity3d下载与安装](#1-1unity3d下载与安装)
*  [2.IDE的准备工作](#2-ide的准备工作)
	- [Rider的安装与配置](#rider的安装与配置)
*  [3.unity3d基础入门](#3unity3d基础入门)
	- [问题](#问题)
	- [插件选择](#插件选择)
*  [4.unity3d进阶](#4-unity3d进阶)
	- [游戏常用的算法](#游戏常用的算法)
	- [进阶知识点](#进阶知识点)
*  [5.服务器方案选择](#5-服务器方案选择)
*  [6.c#语言](#6-c语言)
*  [推荐的书单](#推荐的书单)
*  [学习网站](#学习网站)


## 1 unity3d下载与安装

[unity3官网所有下载地址](https://unity3d.com/cn/get-unity/download/archive)：注意，unity3d个人版与专业版是一个安装文件，区别在于专业版登录时需要license。个人版已经包含了unity3d引擎核心的全部工具，选用这个就行。

[全系列Unity4.x.x到2017.1.0破解Win&Mac!最新Unity2017.1.0p2&4.7.2f1破解](http://www.ceeger.com/forum/read.php?tid=23396):个人感觉专业版破解就是比个人版多了个皮肤，其他功能还是没有，专业版其他功能都需要网络支持。



## 2 IDE的准备工作
c#的ide有以下三种：

*  MonoDevelop，安装自带的跨平台ide。个人感觉不太好用
*  Visual Studio for mac:微软大法好，用过都说吊。但是安装太慢，[给一个离线安装的地址](https://www.coderbusy.com/archives/569.html).
*  JetBrans Rider:跨平台c#的ide。jb公司出品，用过AndroidStudio,WebStorm的自然懂，所以就是你了。

#### Rider的安装与配置

[jetbrains Rider下载地址](https://www.jetbrains.com/rider/)

jetbrains的license server: http://idea.ibdyr.com/

[使用JetBrains Rider EAP开发和调试 Unit](http://blog.csdn.net/u010019717/article/details/60324867)

1.  Unity->Perference->External Tools
2.  找到External Script Editor 下拉列表中 选择 "Browse"
3.  找到~/Application/Rider2017.1
4. 2017版已经自带了unity support插件，无需手动导入了

如何配置git呢？

1.  修改后ctrl+s保存
2. Editor->Project Setting->Editor->Version Control ->Visible Meta Files,新版unity可能已经自动开启了
3.  Editor->Project Setting->Editor->Asset Serializetion ->Force Text
4.  如何更新工程后，unity窗口没有变化，可以选择重启功能或者 Assets->Refresh/Reimport All

参考资料[How to use Git for Unity3D source control?](https://stackoverflow.com/questions/18225126/how-to-use-git-for-unity3d-source-control)



## 3 unity3d基础入门
>这里开始学会如何使用unity3d开发游戏，我们最好是带着问题去学习

#### 问题

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
>脚本命名方面：UI专用的脚本用UI_XXXX,特效专用脚本FX_XXX,行为脚本AC_XXXX
* 如何使用protobuf序列化？
* 脚本的生命周期？
* 短链接www或者WebRequest,长连接KCP/TCP,以及udp的区别，总结分析你？
* 如何用PoolManager或者FastPool用来做对象缓存池
* 

#### 插件选择
* POI：解析excel文件并导入，策划神器
* ConsoleE:console插件
* EasyTouch：摇杆插件，很好用
* tk2d:最火的2d游戏开发插件，比unity2d要优秀，据说。但是目前完全可以用原生unity2d+ugui开发
* DoTWeen：差值动画插件
* ulua或者slua:热更新
* protobuf-net：前端数据序列化库
* SimpleJson：数据序列化库
* Vision Timer(定时器插件)
* FX Maker:粒子特效插件，可以转帧，适合移动平台

#### 基础开发

 
## 4 unity3d进阶
> 从这里开始向着大牛迈进


#### 游戏常用的算法

* 相交性检测
* 无缝地图加载
* aoi
* 游戏资源管理，性能分析，游戏架构

#### 进阶知识点

* 图形学
* 图形学基本原理
* OpenGL


## 5 服务器方案选择

通信建议还是protobuf格式。弱网环境包体更小，更稳定。

|名称|语言|优点|缺点|
|---|---|---|---|
|SmartFox 2X|java|入门简单，商业级服务器，基于java netty为发展框架，client支持flash，unity, ios, android(java), c++. 等等||
|PHP+skynet|pua||
|scut|c#|开源，和前端同样的语言，|同时兼顾了长连接和短链接，结果对长连接的支持不是很好|
|Pomelo|nodejs|网易出品的开源分布式架构|
|Photn|c#|商业级服务器|||

## 6 c#语言

从unity2017开始，使用的script runtime版本是.net Framework3.5 和4.6对应c#语言版本3.0和6.0。
使用的api compatility Level还是.net2.0。
建议ios android用.net 2.0,web端用.net 2.0 subset


.net版本与c#版本对比图如下：

|.net framework	|c# version|	note|	date
|---|---|----|---|
|.net 3.5	|3.0|	vs2008 |	2007-08|
|.net 4.0	|4.0|	vs2010	|2010-04|
|.net 4.5 |5.0|	vs2012/13	|2012-10
.net 4.6	|6.0|	vs2015|	2015-07

#### 必备的知识点

* 事件驱动的编程模型，比如delegate/event ,BeginInvoke




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

## 学习网站

* [unity圣典](http://www.ceeger.com/Manual/):unity api的中文翻译网站，可以作为工具书使用，配置官方api阅读
* [unity官方指南与脚本api](https://docs.unity3d.com/Manual/index.html):官方文档，英文好可以一读
* [unity官方学习教程](https://unity3d.com/cn/learn):有视频，有源码，福利慢慢
* [雨松momo的blog](http://www.xuanyusong.com/archives/3278):通俗易懂，值得一看
* [unity中文论坛](http://forum.china.unity3d.com/forum.php?mod=forumdisplay&fid=56)
*  游戏蛮牛：大而全的网站。





