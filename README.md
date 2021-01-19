# Android-Core-Realm
What you need to know to be a good Android developer

## 目录

| Ⅰ | Ⅱ | Ⅲ | Ⅳ | Ⅴ | Ⅵ | Ⅶ | Ⅷ | Ⅸ | Ⅹ | Ⅺ | Ⅻ | XIII | XIV |
| :--------: | :---------: | :---------: | :---------: | :---------: | :---------:| :---------: | :-------: | :-------: |  :-------: |  :-------: |  :-------: |  :-------: |  :-------: | 
| UI组件 [:beginner:](#UI组件-beginner) | 四大组件 [:computer:](#四大组件-computer) | 动画 [:yin_yang:](#动画-:yin_yang:) | 设计模式 [:checkered_flag:](#设计模式-checkered_flag) | 异步任务机制 [:vertical_traffic_light:](#异步任务机制-vertical_traffic_light) | 自定义View[:rocket:](#自定义View-rocket) | 网络请求[:heart:](#网络请求-heart) | 响应式编程[:monkey:](#响应式编程-monkey) | Kotlin [:fire:](#kotlin-fire) | 进程通信 [:phone:](#进程通信-phone) | 性能优化[:wrench:](#性能优化-wrench) | 优秀第三方控件[:man:](#优秀第三方控件-man) | NDK[:apple:](#NDK-apple) | 拓展[:fork_and_knife:](#拓展-fork_and_knife) |

## 前言:

RecyclerView、Andorid动画、OkHttp与Retrofit的网络请求、多进程、View的绘制流程、事件分发、消息队列、AIDL、Binder、Kotlin等，这类知识对于要成为一位优秀Android工程师的人来说是必须完全掌握的，同时他也是能鉴别高级和初中级工程师的一块试金石。因此，为了更好将各个知识层面的知识体系更好融合在一起，笔者创建了Android-Core-Realm这个项目，希望带领读者掌握Android系统架构中各个核心技能。

> OkHttp与Retrofit是当前主流网络请求框架，view的绘制是我们自定义控件的理论基础，只有掌握了view是如何绘制的才能个性化的自定义控件；事件分发一直是Android开发的难点之一，也是必须掌握的；关于handler机制也是android的一块难点，因为包括Asynctask、系统启动、Intentservice等底层都是通过handler来实现的，所以掌握后handler机制不仅能提高你的实战开发能力，更能让你系统的了解整个android系统运作的情况;binder是Android系统进程间通信最重要的手段之一，现阶段app的发展离不开多进程的运用，经常会启动例如定位、推送等需要在后台开启动的进程来来保证主进程的内存运行；所以合理的使用多进程也是十分必要的；性能优化是Android细分领域中最难且也是知识面涉及最深和最广的方向之一；Flutter、热修复、插件化等是发展潮流需要。

- 软技能(已完成)
> [(建议精读)学习之力 — 提高学习效率99%的灵魂秘籍！](https://blog.csdn.net/m0_37796683/article/details/111991593)

- Andorid核心思维导图总览(持续更新……)
> [点击查看大图](https://github.com/FollowExcellence/Android-Core-Realm/blob/main/AndoridCorePlan.png)

## ⅠUI组件 :beginner:

### 布局控件

> [ConstraintLayout约束布局](https://blog.csdn.net/m0_37796683/article/details/103366626)
- 作为一款强大的调整View位置和大小的ViewGroup被Google所推荐，它能在复杂布局中有效降低布局层级，提高性能，使用更加灵活。

### RecyclerView系列

Android5.0之后Google推出了新的列表控件RecyclerView，代替了经典的ListView，是一个强大的滑动组件，拥有item的复用回收功能，更加高级和灵活。

> [深入理解 RecyclerView (一、基础篇)](https://blog.csdn.net/m0_37796683/article/details/103697121)
- RecyclerView的基础使用、网格布局、瀑布流布局

> [深入理解 RecyclerView (二、功能篇)](https://blog.csdn.net/m0_37796683/article/details/103711941)
- RecyclerView的ItemType(不同条目类型)

> [深入理解 RecyclerView (三、功能篇)](https://blog.csdn.net/m0_37796683/article/details/103990481)
- RecyclerView的ItemDecoration分割线、增删item动画效果、拖拽和侧滑删除功能

> [深入理解 RecyclerView (四、封装篇)](https://blog.csdn.net/m0_37796683/article/details/103866299)
- RecyclerView的自定义点击事件、万能ViewHolder和Adapter简单封装

> [深入理解 RecyclerView (五、绘制篇)](https://blog.csdn.net/m0_37796683/article/details/104864318)
- 源码剖析RecyclerView的绘制流程

> [深入理解 RecyclerView (六、滑动篇)](https://blog.csdn.net/m0_37796683/article/details/104951780)
- 源码剖析RecyclerView的滑动原理

> [深入理解 RecyclerView (七、滑动篇)](https://blog.csdn.net/m0_37796683/article/details/105065358)
- 源码剖析RecyclerView的嵌套滑动机制

> [深入理解 RecyclerView (八、缓存篇)](https://blog.csdn.net/m0_37796683/article/details/105141373)
- 源码剖析RecyclerView的回收复用缓存机制

> [深入理解 RecyclerView (九、自定义篇)](https://blog.csdn.net/m0_37796683/article/details/105138868)
- 参考RecyclerView的LinearLayoutManager原理自定义LayoutManager

## Ⅱ 四大组件 :computer:

### Activity 

Activity是Android应用的四大组件之一，它负责管理Android应用的用户界面。

> [Activity系列(一、基础篇)](https://blog.csdn.net/m0_37796683/article/details/105243356)
- Activity：创建步骤、清单文件注册、显式隐式意图、数据传递

> [Activity系列(二、启动篇)](https://blog.csdn.net/m0_37796683/article/details/103335332)
- Activity的四种启动模式(图解实例和场景使用)

## Ⅲ Andorid动画系列 :yin_yang:

Android动画有两种类型的动画View Animation(视图动画)和Property Animation(属性动画)。

### View动画

> [Android动画(一、基础篇)](https://blog.csdn.net/m0_37796683/article/details/90293418)
- 补间动画alpha、scale、translate、rotate、set的xml属性及用法

> [Android动画(二、基础篇)](https://blog.csdn.net/m0_37796683/article/details/90376533)
- 代码动态实现补间动画alpha、scale、translate、rotate、set、插值器动画&属性详解

### 属性动画

> [Android动画(三、基础篇)](https://blog.csdn.net/m0_37796683/article/details/90440702)
- 属性动画ValueAnimator的基本使用

> [Android动画(四、基础篇)](https://blog.csdn.net/m0_37796683/article/details/90483462)
- 属性动画ObjectAnimator基本使用以及属性详解

> [Android动画(五、进阶篇)](https://blog.csdn.net/m0_37796683/article/details/90607428)
- 插值器(Interpolator)、计算器(Evaluator)、ValueAnimator的ofObject用法等相关知识

> [Android动画(六、组合篇)](https://blog.csdn.net/m0_37796683/article/details/90645047)
- 组合动画AnimatorSet和PropertyValuesHolder的使用

### 动画原理

> [Android动画(七、原理篇)](https://blog.csdn.net/m0_37796683/article/details/90904394)
- 补间动画(Tween Animation)的运行原理

> [Android动画(八、原理篇)](https://blog.csdn.net/m0_37796683/article/details/91534275)
- 属性动画的原理

## Ⅳ 常用设计模式 :checkered_flag:

设计模式代表了最佳的实践，是一套被反复使用，多数人知晓，经过分类编目，代码设计经验的总结。使用设计模式是为了重用代码，让代码更容易被人理解，保证代码可靠性。设计模式提供了软件开发过程中面临的一些问题的最佳解决方案，非常重要。

### 单例模式

> [设计模式(一、单例模式)](https://blog.csdn.net/m0_37796683/article/details/103203266)
- 单例模式的几种实现方式

## Ⅴ 异步任务机制 :vertical_traffic_light:

Andorid中的重点难点

### Handler消息机制

> [深入理解Android消息机制](https://blog.csdn.net/m0_37796683/article/details/100524852)
- 源码剖析Handler消息机制

### Thread和线程池

> [深入理解Android线程池](https://blog.csdn.net/m0_37796683/article/details/103054999)
- Android 线程池的使用和原理

> [Thread线程停止的几种方式](https://blog.csdn.net/m0_37796683/article/details/103216759)
- 如何正确地停止线程？

## Ⅵ 自定义View :rocket:

View的绘制是我们自定义控件的理论基础，绘制原理、滑动原理、弹性滑动、滑动冲突、measure、layout和draw等，掌握才能绘制个性化的自定义控件，事件分发一直是Android开发的难点之一。

### View的工作原理

### View的事件分发机制

[深入理解Android事件分发机制(未完成)]

### 自定义控件

> [自定义View(一、基础篇)](https://blog.csdn.net/m0_37796683/article/details/97810538)
- 自定义控件的初始化

## Ⅶ 网络请求 :heart:

OKHttp是一款优秀HTTP框架，retrofit是现在比较流行的网络请求封装框架，可以理解为okhttp的加强版，底层封装了Okhttp。

### OkHttp

> [OkHttp(一、基础篇)](https://blog.csdn.net/m0_37796683/article/details/101029208)
- OkHttp的介绍和使用
> [OkHttp(二、原理篇)](https://blog.csdn.net/m0_37796683/article/details/101306070)
- 深入源码解析OkHttpClient、dispatcher调度器、Intercepoter拦截器

### Retrofit

> [Retrofit(一、基础篇)](https://blog.csdn.net/m0_37796683/article/details/90702095)
- Retrofit的介绍和使用

## Ⅷ 响应式编程 :monkey:
 
### RxJava 

一个优秀的异步操作库，简洁、优雅、强大的操作符。（一个在 JVM 上使用可观测的序列来组成异步的，基于事件的程序的库）

> [RxJava2详解(一)](https://blog.csdn.net/m0_37796683/article/details/102525484)
- 详细介绍了RxJava的使用（基本创建、快速创建、延迟创建等操作符）

> [RxJava2详解(二)](https://blog.csdn.net/m0_37796683/article/details/102609400)
- RxJava转换、组合、合并等操作符的使用

> [RxJava2详解(三)](https://blog.csdn.net/m0_37796683/article/details/102680215)
- RxJava延迟、do相关、错误处理等操作符的使用

> [RxJava2详解(四)](https://blog.csdn.net/m0_37796683/article/details/102718718)
- RxJava过滤、其他操作符的使用

## Ⅸ Kotlin :fire:

Android 的官方开发语言，能很好兼容Java，简洁优雅务实安全，函数式编程。

### Kotlin基础
> [Kotlin基础「一」](https://blog.csdn.net/m0_37796683/article/details/106574861)
- 你了解Kotlin的let，with，run，apply，also作用域函数的区别吗？

> [Kotlin基础「二」](https://blog.csdn.net/m0_37796683/article/details/107090174)
- 变量(var与val)、常量、注释

> [Kotlin基础「三」](https://blog.csdn.net/m0_37796683/article/details/107125802)
- 数据类型（数值类型，布尔类型，字符类型，字符串类型，数组类型）

> [Kotlin基础「四」](https://blog.csdn.net/m0_37796683/article/details/107205359)
- 逻辑控制语句（if、for、when、while、return、break、continue）

> [Kotlin基础「五」](https://blog.csdn.net/m0_37796683/article/details/107515659)
- 可空类型?，空安全?.，空值合并?:，非空断言!!，类型安全转换as?

> [Kotlin基础「六」](https://blog.csdn.net/m0_37796683/article/details/107562219)
- 函数的声明和使用

> [Kotlin基础「七」](https://blog.csdn.net/m0_37796683/article/details/107684706)
- 类和继承

> [Kotlin基础「八」](https://blog.csdn.net/m0_37796683/article/details/107759662)
- 属性与字段（Getter()与Setter()，后备字段field）

> [Kotlin基础「九」)](https://blog.csdn.net/m0_37796683/article/details/107957844)
- 包与导入(Packages and Imports)

> [Kotlin基础「十」](https://blog.csdn.net/m0_37796683/article/details/107964620)
- 接口与函数接口（Functional (SAM) interfaces）

> [Kotlin基础「十一」](https://blog.csdn.net/m0_37796683/article/details/107987178)
- 可见性修饰符（private、protected、internal、public）

> [Kotlin基础「十二」](https://blog.csdn.net/m0_37796683/article/details/108011223)
- 扩展Extensions（扩展函数与属性）

> [Kotlin基础「十三」](https://blog.csdn.net/m0_37796683/article/details/108078923)
- 数据类（Data Classes）

> [Kotlin基础「十四」](https://blog.csdn.net/m0_37796683/article/details/108149524)
- 密封类（Sealed Classes）

> [Kotlin基础「十五」](https://blog.csdn.net/m0_37796683/article/details/108202337)
- 泛型

> [Kotlin基础「十六」](https://blog.csdn.net/m0_37796683/article/details/108863997)
- 嵌套和内部类

> [Kotlin基础「十七」](https://blog.csdn.net/m0_37796683/article/details/108872675)
- 枚举类（enum class）

> [Kotlin基础「十八」](https://blog.csdn.net/m0_37796683/article/details/109048386)
- object（对象表达式和对象声明）

> [Kotlin基础「十九」](https://blog.csdn.net/m0_37796683/article/details/109100517)
- 类型别名（type alias）

> [Kotlin基础「二十」](https://blog.csdn.net/m0_37796683/article/details/109224751)
- 内联类（Inline classes）

> [Kotlin基础「二十一」](https://blog.csdn.net/m0_37796683/article/details/109745526)
- 委托和委托属性详解

> [Kotlin基础「二十二」](https://blog.csdn.net/m0_37796683/article/details/110234137)
- Lambdas和高阶函数详解

> [Kotlin基础「二十三」](https://blog.csdn.net/m0_37796683/article/details/111051521)
- 引用的使用 :: （类引用、属性引用、函数引用、绑定引用）

> [Kotlin基础「二十四」](https://blog.csdn.net/m0_37796683/article/details/108646530)
- 注解：声明、应用、元注解


(未完成)

### Kotlin协程

### Jetpack组件

## Ⅹ进程通信 :phone:

Android系统进程间通信最重要的手段之一

## Ⅺ 性能优化 :wrench:

性能优化是Android细分领域中最难且也是知识面涉及最深和最广的方向之一

> [最全面&详细的性能优化攻略](https://blog.csdn.net/m0_37796683/article/details/102590141)
- 包含内存优化、内存泄漏、绘制优化、布局优化、图片优化、APK优化、多线程优化、列表优化等

## Ⅻ 优秀第三方控件 :man:

### 图片加载：Glide

- 优秀的图片加载库，Android使用最广泛的图片加载框架。

### 事件总线：EventBus

使用扩展的观察者模式实现的组件间通信框架，广播的替代者。EventBus能够简化应用组件间的通信，解耦(有效分离)事件的发送者和接收者，避免复杂和容易出错的依赖和生命周期问题，开销小，代码更优雅。

> [EventBus3.2详解和使用(一)](https://blog.csdn.net/m0_37796683/article/details/105585228)
- EventBus普通事件和粘性事件的使用

> [EventBus3.2详解和使用(二)](https://blog.csdn.net/m0_37796683/article/details/105774997)
- EventBus三要素、线程模式、优先级和AndroidEventBus的使用

> [EventBus3.2详解和使用(三)](https://blog.csdn.net/m0_37796683/article/details/105820728)
- 源码剖析EventBus内部原理

## XIII NDK :apple: (敬请期待)

### JNI

## XIV 拓展 :fork_and_knife: (敬请期待)

### 热修复

### Flutter

### 插件化

### 组件化

#### 笔者有话说

在Android源码中最重要的三个类：ActivityManagerService／PackageManagerService／View，推荐大家去阅读下这部分的源码，阅读源码能提高我们今后设计架构自己代码的能力，同时也能从底层了解整个android系统的运行原理，其他一些比如主线程的消息循环、主线程如何和AMS如何跨进程交互、SystemServer进程中的各种Service的工作方式、AsyncTask的工作原理等。这些知识也是作为一个Android高级开发工程师必须掌握的，不能整天沉溺于ui和四大组件的交互，要站在更高的角度去考虑Android的有些问题。

欢迎在 Issue 中提交对本仓库的改进建议~

## 版权声明

* 所有原创文章(未进行特殊标识的均属于原创) 的著作权属于 **Sumiya**。
* 所有译文文章(标题注明`[译]`的所有文章) 的原文著作权属于原作者，译文著作权属于 **Sumiya**。

#### 转载注意事项

除注明外，所有文章均采用 [Creative Commons BY-NC-ND 4.0（自由转载-保持署名-非商用-禁止演绎）](http://creativecommons.org/licenses/by-nc-nd/4.0/deed.zh)协议发布。

您可以在非商业的前提下免费转载，但同时您必须：

* 保持文章原文，不作修改。
* 明确署名，即至少注明 `作者：Sumiya` 字样以及文章的原始链接。
* 商业用途请以邮件方式联系本人。
* 微信公众号转载一律不授权 `原创` 标志。

### About me

- #### 微信：`SUM_817`
- #### Email：`su_mingyan@163.com`
- #### Blog：[https://blog.csdn.net/m0_37796683/](https://blog.csdn.net/m0_37796683/)


## 赞赏

如果这个库对您有很大帮助，您愿意支持这个项目的进一步开发和持续维护。您可以扫描下面的二维码，打赏我一颗糖果或者一杯咖啡，非常感谢您的捐赠。祝您百尺竿头更进一步！

<div align="center">
<img src="https://github.com/FollowExcellence/Android-Core-Realm/blob/main/alpay.jpg" width=20%>
<img src="https://github.com/FollowExcellence/Android-Core-Realm/blob/main/wechatpay.jpg" width=20%>
</div>

