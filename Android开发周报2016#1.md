# Android开发周报：Android将使用OpenJDK、React Native详解


---

摘要：谷歌的移动操作系统正在将原先基于Harmony实现的Java库切换到OpenJDK。Android6.0的市场占有率依然很低，发布三个月却只有0.7%。本期周报为大家带来了Xposed详解、App插架化实现等多篇干货文章，并且为大家推荐了FileDownloader、GalleryFinal等优秀开源项目。

####新闻
---
1. [《Android将使用OpenJDK》](http://www.infoq.com/cn/news/2016/01/android-openjdk)：据[Hacker News](https://news.ycombinator.com/item?id=10803775)根据Android的一次源码提交表明，谷歌的移动操作系统正在将原先基于Harmony实现的Java库切换到OpenJDK。在2010年收购Sun之后，Oracle起诉谷歌在Android上使用Java代码侵犯版权和专利权。谷歌起初赢得了官司，陪审团判定Java API没有版权，但联邦巡回法庭部分地推翻了这项裁决，认为API有版权。美国最高法院不希望看到这种情况，就将其发给了一个下级法院。那个过程目前还在继续。
2. [《发布三个月 Android 6.0占比仅有0.7%》](http://mobile.pconline.com.cn/742/7422965.html)：谷歌在去年九月底推出了Android 6.0系统，并于十月初放出，但直到现在这个版本的系统占比也是十分的低。近日谷歌公布了最新的Android系统版本最新数据，占据份额最多的依旧是Android 4.4，而Android 6.0只有0.7%。
3. [《谷歌真要回来了：中国版Google Play惊现！》](http://news.mydrivers.com/1/465/465515.htm)：从去年开始，谷歌服务回归中国市场的传闻就一直没有停断过。近日，联想移动业务总裁陈旭东的一番表态坐实了传言，他表示：“谷歌服务肯定会重新进入中国市场，今年无论如何都会回来。”，另外有多名网友曝光了一张Google Play帮助页面的截图，里面赫然出现了“中国版Google Play”的字样，再次从侧面证实以上消息。


####教程
---
1. [《深入理解Android（三）：Xposed详解》](http://www.infoq.com/cn/articles/android-in-depth-xposed)：从事Android开发的同学应该都知道Xposed这个神一样的框架。Xposed功能强大，它不仅仅具有插件加载功能，而且可以Hook Android Java虚拟机。当然，Xposed也有缺点，比如当我们开发插架时，每次编译后都需要重新启动设备。Xposed强大，我们可以学习其中的精髓，并且可以把它的思想和技术用到自己的插件加载模块里，本文详细分析了Xposed的工作原理。
2. [《React Native For Android源码分析-JS如何调用Native的代码》](http://zhuanlan.zhihu.com/program-life/20464825)：React Native是2015年最有影响力的开源项目之一。目前国内对于React Native的实践还比较少，估计也只有BAT等一些知名厂商在尝试。所以React Natvie的学习资料比较少。本文是一篇介绍React Native For Android源码的文章，详细分析了JS调用Native代码的过程，是我们学习React Native的优秀教程。
3. [《微信Android客户端架构演进之路》](http://www.infoq.com/cn/articles/wechat-android-app-architecture)：去年本文作者在InfoQ举办的ArchSummit深圳2014的架构师峰会上，分享了微信Android客户端的架构演进史。可以说，这是一个典型的Android应用在从小到大的成长过程中的”踩坑”与“填坑”的历史。互联网的变化速度如此之快。2015年底，作者重新和大家回顾了微信客户端架构的演进过程，以及其背后的开发团队、流程的变化与思考。
4. [《Android应用坐标系统全面详解》](http://blog.csdn.net/yanbober/article/details/50419117)：很多人可能不屑一顾Android的坐标系，但是如果你想彻底学会自定义控件，了解Android各种坐标系及一些API的坐标含义，绝对算一个小而不可忽视的技能。所谓Android自定义View那几大主要onXXX()方法的重写，其实大多数都是在处理坐标逻辑运算。说到Android坐标系其实就是一个三维坐标，Z轴向上，X轴向右，Y轴向下。这三维坐标的点处理就能构成Android丰富的界面或者动画等效果，所以Android坐标系在整个Android界面中算是盖楼房的尺寸草图。本文详解了Android中的坐标系统。
5. [《Gradle for Android之Build.gradle入门》](http://segmentfault.com/a/1190000004234712)：当我们创建一个新的工程，Android studio会默认为我们创建三个gradle文件，两个build.gradle，一个settings.gradle，build.gradle分别放在了根目录和moudle目录下。但这些gradle文件分别是干什么用的？很多同学对于这一点并不清楚。本文讲解了Gradle在一些基础知识，以及Android Studio的项目构建过程。
6. [《途牛Android App的插件实现》](http://mp.weixin.qq.com/s?__biz=MzAwOTE0ODEwMQ==&mid=401731625&idx=1&sn=9bf2bacfbba43ba9dc7b2e854b64e66c&scene=23&srcid=1231ni0s2Y0OMfYSoNhkkJ47#rd&ADUIN=289832127&ADSESSION=1451551778&ADTAG=CLIENT.QQ.5425_.0&ADPUBNO=26509)：途牛的插件化是基于[dynamic-load-apk](https://github.com/singwhatiwanna/dynamic-load-apk)实现的。定义了宿主和插件的通信方式，使得两者能够互相唤起对方的页面，调用彼此的功能。同时对activity的启动方式singletask等进行了模式实现，并增加了对Service的支持等。总之使得插件开发最大限度的保持着原有的Android开发习惯。本文来自途牛技术中心，详细分析了生产环境下插件化的实现方式。
7. [《Android应用启动优化:一种DelayLoad的实现和原理（下篇）》](http://androidperformance.com/2015/12/29/Android%E5%BA%94%E7%94%A8%E5%90%AF%E5%8A%A8%E4%BC%98%E5%8C%96-%E4%B8%80%E7%A7%8DDelayLoad%E7%9A%84%E5%AE%9E%E7%8E%B0%E5%92%8C%E5%8E%9F%E7%90%86-%E4%B8%8B%E7%AF%87.html)：本文是作者介绍Android应用启动优化的第二篇文章，[这里](http://www.androidperformance.com/2015/11/18/Android-app-lunch-optimize-delay-load.html)是第一篇。在Android 开发中，应用启动速度是一个非常重要的点，应用启动优化也是一个非常重要的过程。延迟加载的实现非常简单，但是其中的原理却比较复杂，涉及到Handler、Activity启动过程等多个知识点。本文利用多个工具，详细分析了延迟加载的原理。

####开源项目
---
1. [FileDownloader](http://androidone.io/info_10102.html)：FileDownloader是一款Android 文件下载引擎，其特点是稳定、高效、且简单易用。FileDownloader支持高并发、独立进程及自动断点续传等功能。
2. [Small](https://github.com/wequick/Small)：这是一个轻巧的跨平台插件化框架。Small的所有插件支持内置于宿主包中；插件编码、布局编写方式与独立应用开发无异；插件代码调试与整包开发无异。目前Small已支持Android、iOS以及html5插件，并且三者之间可以通过同一套javascript接口进行通信。
3. [GalleryFinal](http://androidone.io/info_10103.html)：这是一个Android自定义相册项目，实现了拍照、图片选择（单选/多选）、 裁剪（单/多裁剪）、旋转、ImageLoader无绑定任由开发者选 择、功能可配置、主题样式可配置。
####工具
----
1. [recompress-apk](https://github.com/hyongbai/recompress-apk)：这是一个可压缩已签名的apk的体积的脚本，且不会破坏签名。测试可把微信从32MB压到30MB。如果资源占比更大的话，效果更明显。
2. [android-plus-plus](https://github.com/webbju/android-plus-plus)：Android++是在Vistual Studio上进行Android开发的解决方案。Android++主要是针对基于NDK的开发，但也支持部署、资源管理及Java编译等。

####图书
----
1. [《RxJava-Essentials-CN》](https://github.com/yuxingxin/RxJava-Essentials-CN)：这是一本关于RxJava的书箱，翻译自Ivan.Morgillo所写的《RxJava Essentials》。


