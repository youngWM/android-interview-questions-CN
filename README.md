<p align="center">
<img alt="" src="https://github.com/youngWM/android-interview-questions-CN/blob/master/assets/banner-android-interview-questions.png">
</p>
 
# 安卓面试题

> Android 面试问题 - 你的 Android 面试备忘单

---

# 序
### 由[Amit Shekhar](https://github.com/amitshekhariitbhu)编写和维护，他有接受许多 Android 开发人员面试和顶级公司面试的经验。

### Amit Shekhar 自我介绍

大家好，我是`Amit Shekhar`，我指导过很多开发人员，他们的努力让他们获得了高薪技术工作，帮助许多科技公司解决了他们独特的问题，并创建了许多被顶级公司使用的开源库。我热衷于通过开源、博客和视频分享知识。

您可以通过以下方式与我联系：

- [Twitter](https://twitter.com/amitiitbhu)
- [YouTube](https://www.youtube.com/@amitshekhar)
- [LinkedIn](https://www.linkedin.com/in/amit-shekhar-iitbhu)
- [GitHub](https://github.com/amitshekhariitbhu)

### 为 `Android` 面试做准备的高质量视频 - [Amit Shekhar YouTube Channel](https://www.youtube.com/@amitshekhar)

### 为 `Android` 面试做准备的高质量博客  [Blog by Amit Shekhar](https://amitshekhar.me/blog)

#### **获取指导: [amitshekhar.me](https://amitshekhar.me)**

<br>

---
<br>

## 目录

* [一.Kotlin for Android 面试须知](#一.Kotlin-for-Android-面试须知)
* [二.Android 核心](#二.Android核心)
* [三.Android 库](#三.Android-Libraries-安卓库)
* [四.Android Architecture 安卓架构](#四.Android Architecture 安卓架构)
* [五.Android 设计问题](#五.Android Design Problem 安卓设计问题)
* [六.Android Unit Testing 安卓单元测试](#六.Android Unit Testing 安卓单元测试)
* [七.Android Tools And Technologies 安卓工具和技术](#七.Android Tools And Technologies 安卓工具和技术)
* [八.Java 和 Kotlin](#八.Java 和 Kotlin)
* [九.Kotlin 协程](#九.Kotlin 协程)
* [十.Kotlin Flow API](#十.Kotlin Flow API)
* [十一.Jetpack Compose Jetpack](#十一.Jetpack Compose)
* [十二.Other Topics 其他主题](#十二.Other Topics 其他主题)
* [十三.Data Structures and Algorithms 数据结构和算法](#十三.Data Structures and Algorithms 数据结构和算法)

<br>

---
<br>

## 一.Kotlin for Android 面试须知

- [掌握 kotlin 协程](https://github.com/youngWM/android-interview-questions-CN/blob/master/Kotlin%20for%20Android%20%E9%9D%A2%E8%AF%95%E9%A1%BB%E7%9F%A5/%E6%8E%8C%E6%8F%A1%20Kotlin%20%E5%8D%8F%E7%A8%8B.md) -Mastering Kotlin Coroutines
- [精通 Kotlin 协程](https://amitshekhar.me/blog/kotlin-coroutines) -
- [kotlin 协程中 Launch 与 Async 的比较](https://amitshekhar.me/blog/launch-vs-async-in-kotlin-coroutines)-Launch vs Async in Kotlin Coroutines
- [kotlin 协程中的程序调度者 Dispatchers](https://amitshekhar.me/blog/dispatchers-in-kotlin-coroutines) -Dispatchers in Kotlin Coroutines
- [coroutineScope 对比 supervisorScope](https://amitshekhar.me/blog/coroutinescope-vs-supervisorscope) - coroutineScope vs supervisorScope
- [什么是 Kotlin 中的 Flow API?](https://amitshekhar.me/blog/flow-api-in-kotlin) - 什么是 Kotlin 中的 Flow API？
- [长时间运行的任务与 Kotlin Flow 并行](https://amitshekhar.me/blog/long-running-tasks-in-parallel-with-kotlin-flow) -Long-running tasks in parallel with Kotlin Flow 
- [Kotlin Flow 中的重试运算符](https://amitshekhar.me/blog/retry-operator-in-kotlin-flow) -Retry Operator in Kotlin Flow 
- [回调到 Kotlin 中的协程](https://amitshekhar.me/blog/callback-to-coroutines-in-kotlin) - Callback to Coroutines in Kotlin
- [callbackFlow - 回调 Kotlin 中的 Flow API](https://amitshekhar.me/blog/callback-to-flow-api-in-kotlin) - callbackFlow - Callback to Flow API in Kotlin
- [StateFlow 和 SharedFlow](https://amitshekhar.me/blog/stateflow-and-sharedflow) - StateFlow and SharedFlow
- [冷流与热流](https://amitshekhar.me/blog/cold-flow-vs-hot-flow) - Cold Flow vs Hot Flow
- [Retrofit 使用 Kotlin Flow](https://amitshekhar.me/blog/retrofit-with-kotlin-flow) - Retrofit with Kotlin Flow
- [Room 数据库使用 Kotlin Flow](https://amitshekhar.me/blog/room-database-with-kotlin-flow) - Room Database with Kotlin Flow
- [从 Kotlin 中的数组中删除重复项](https://amitshekhar.me/blog/remove-duplicates-from-an-array-in-kotlin) - Remove duplicates from an array in Kotlin
- [Kotlin 中的 JvmStatic 注解](https://www.youtube.com/watch?v=qBBbOhY_pv4) - JvmStatic Annotation in Kotlin
- [Kotlin 中的 JvmOverloads 注解](https://www.youtube.com/watch?v=fHGsBV9Za8M) - JvmOverloads Annotation in Kotlin
- [ Kotlin 中的 JvmField 注解](https://www.youtube.com/watch?v=bx8OZcMbeUE) - JvmField Annotation in Kotlin
- [Kotlin 中的内联函数](https://www.youtube.com/watch?v=GLLI8h67ryo) - inline function in Kotlin
- [Kotlin 中的 noinline](https://amitshekhar.me/blog/noinline-in-kotlin) - noinline in Kotlin
- [Kotlin 中的 crossinline](https://amitshekhar.me/blog/crossinline-in-kotlin) - crossinline in Kotlin
- [Kotlin 中的 lateinit vs lazy](https://amitshekhar.me/blog/lateinit-vs-lazy-in-kotlin) - lateinit vs lazy in Kotlin
- [Kotlin 中的初始化块](https://www.youtube.com/watch?v=cb3jOFozJns) - init block in Kotlin
- [Kotlin 中 == 和 === 的区别](https://amitshekhar.me/blog/structural-and-referential-equality-in-kotlin) - Difference between == and === in Kotlin
- [Retrofit with Kotlin 协程](https://amitshekhar.me/blog/retrofit-with-kotlin-coroutines) - Retrofit with Kotlin Coroutines
- [在 Kotlin 中使用 const 的优点](https://www.youtube.com/watch?v=3G49ivVxfkU) - Advantage of using const in Kotlin
- [Kotlin Coroutines 中的挂起函数](https://amitshekhar.me/blog/suspend-function-in-kotlin-coroutines) - suspend function in Kotlin Coroutines
- [Kotlin 中的高阶函数和 Lambda](https://amitshekhar.me/blog/higher-order-functions-and-lambdas-in-kotlin) - Higher-Order Functions and Lambdas in Kotlin
- [使用 Kotlin 协程的并行多个网络调用](https://amitshekhar.me/blog/parallel-multiple-network-calls-using-kotlin-coroutines) - Parallel Multiple Network Calls Using Kotlin Coroutines
- [将列表转换为map的 associateBy](https://amitshekhar.me/blog/associateby-list-to-map-in-kotlin) - Kotlin Collection Functions - associateBy that converts a list into a map
- [分区 - Kotlin 中的过滤函数](https://amitshekhar.me/blog/partition-filtering-function-in-kotlin) - partition - filtering function in Kotlin
- [Kotlin 中的中缀符号](https://amitshekhar.me/blog/infix-notation-in-kotlin) - Infix notation in Kotlin
- [kotlin 中的关键词 Open](https://amitshekhar.me/blog/open-keyword-in-kotlin) - Open keyword in Kotlin
- [Kotlin 中的伴随对象](https://amitshekhar.me/blog/companion-object-in-kotlin) - Companion object in Kotlin
- [Kotlin Multiplatform 如何工作？](https://amitshekhar.me/blog/how-does-the-kotlin-multiplatform-work) - How does the Kotlin Multiplatform work?


<br>

---
<br>

### 二.Android核心

<br>

#### 基础

* **为什么 Android 应用程序会滞后？**[英文资料](https://amitshekhar.me/blog/android-app-lag)- Why does an Android App lag?

* **什么是`Context`？它是如何使用的？** - [Android 应用程序中的上下文](https://amitshekhar.me/blog/context-in-android-application) -What is `Context`? How is it used?

* **谈谈所有的 Android 应用程序组件** - [英文资料](https://developer.android.com/guide/components/fundamentals.html#Components)-Tell all the Android application components

* **Android 应用程序的项目结构什么是？** - [英文资料](https://developer.android.com/studio/projects) - What is the project structure of an Android Application?

* **什么是 AndroidManifest.xml？**

* **什么是 `Application` 类?**
    - Android 中的 `Application` 类是 Android 应用程序中的基类，它包含所有其他组件，例如活动和服务。当您的应用程序/程序包的进程被创建时，`Application` 类或 `Application` 类的任何子类在任何其他类之前被实例化。
  （The Application class in Android is the base class within an Android app that contains all other components such as activities and services. The Application class, or any subclass of the Application class, is instantiated before any other class when the process for your application/package is created.）

<br>

---
<br>

#### Activity 和 Fragment 活动和片段

* **为什么建议只使用默认构造函数来创建一个`Fragment`？** - [英文资料](https://www.youtube.com/watch?v=CitBt0FZFIc)

* **什么是`Activity`？它的生命周期？** - What is `Activity` and its lifecycle?

* **`onCreate()` 和 `onStart()` 有什么区别** - What is the difference between `onCreate()` and `onStart()`

* **当没有 `onPause()` 和 `onStop()` 的活动只调用 `onDestroy` 时？  ** - [英文资料](https://www.youtube.com/watch?v=B2kY_ckZa-g) - When only onDestroy is called for an activity without onPause() and onStop()?

* **为什么我们需要在`Activity`类的`onCreate()`中调用`setContentView()`？** - [英文资料](https://www.youtube.com/watch?v=U1aHAt7XC5I) - Why do we need to call setContentView() in onCreate() of Activity class?

* **`Activity`中的 `onSavedInstanceState()` 和 `onRestoreInstanceState()` 是什么？** - What is `onSavedInstanceState()` and `onRestoreInstanceState()` in activity?
    - `onSavedInstanceState()` - 此方法用于在暂停活动之前存储数据。 This method is used to store data before pausing the activity.
    - `onRestoreInstanceState()` - 此方法用于在销毁后重新创建活动时恢复活动的已保存状态。因此，`onRestoreInstanceState()` 接收包含实例状态信息的包。This method is used to recover the saved state of an activity when the activity is recreated after destruction. So, the onRestoreInstanceState() receive the bundle that contains the instance state information.

* **什么是`Fragment` 和 它的生命周期。** What is `Fragment` and its lifecycle.

* **什么是“启动模式” launchMode ？** - [英文资料](https://amitshekhar.me/blog/singletask-launchmode-in-android) and [singleTask launchMode in Android](https://youtu.be/WYkQEnm4jeI) What are "launchMode"?

* **`Fragment`和`Activity`有什么不一样？说明两者的关系** - [英文资料](https://stackoverflow.com/questions/10478233/why-fragments-and-when-to-use-fragments-instead-of-activities) What is the difference between a `Fragment` and an `Activity`? Explain the relationship between the two.

* **什么时候应该使用 `Fragment` 而不是 `Activity`？** - When should you use a Fragment rather than an Activity?
    - 当您有一些 UI 组件要在各种活动中使用时。 When you have some UI components to be used across various activities
    - 当多个视图可以显示viewpage一样。 When multiple view can be displayed side by side just like viewPager

* **`FragmentPagerAdapter` 和 `FragmentStatePagerAdapter` 有什么区别？** What is the difference between `FragmentPagerAdapter` vs `FragmentStatePagerAdapter`?
    - `FragmentPagerAdapter`: 用户访问的每个片段都会存储在内存中，但视图会被销毁。重新访问页面时，将创建视图而不是片段的实例。 Each fragment visited by the user will be stored in the memory but the view will be destroyed. When the page is revisited, then the view will be created not the instance of the fragment.
    - `FragmentStatePagerAdapter`: 这里的fragment实例在用户不可见时会被销毁，fragment的保存状态除外。 Here, the fragment instance will be destroyed when it is not visible to the user, except the saved state of the fragment.

* **在 backstack 中添加/替换 fragment有什么区别？** - [英文资料](https://stackoverflow.com/questions/24466302/basic-difference-between-add-and-replace-method-of-fragment/24466345) - What is the difference between adding/replacing fragment in backstack?

* **你将如何在两个 `Fragment` 之间进行通信？** How would you communicate between two Fragments?

* **什么是保留`Fragment`？** What is retained `Fragment`?
    - 默认情况下，当发生配置更改时，`Fragment` 会与其父 `Activity` 一起被销毁和重新创建。调用 `setRetainInstance(true)` 允许我们绕过这个销毁和重新创建循环，向系统发出信号以在重新创建活动时保留片段的当前实例。By default, Fragments are destroyed and recreated along with their parent Activity’s when a configuration change occurs. Calling setRetainInstance(true) allows us to bypass this destroy-and-recreate cycle, signaling the system to retain the current instance of the fragment when the activity is recreated.

* **`addToBackStack()`提交fragment事务的目的是什么？** - What is the purpose of `addToBackStack()` while commiting fragment transaction?
    - 通过调用 `addToBackStack()`，将替换事务保存到后退堆栈，这样用户可以通过按“后退”按钮来撤销事务并返回前一个片段。By calling addToBackStack(), the replace transaction is saved to the back stack so the user can reverse the transaction and bring back the previous fragment by pressing the Back button. For more [英文资料](https://stackoverflow.com/questions/22984950/what-is-the-meaning-of-addtobackstack-with-null-parameter)

<br>

---
<br>

#### Views 和 ViewGroups 视图和视图组

* **Android 中`View` 是什么？** What is `View` in Android?

* **`View.GONE`和`View.INVISIBLE`之间的区别？** - [英文资料](https://stackoverflow.com/questions/11556607/android-difference-between-invisible-and-gone) Difference between `View.GONE` and `View.INVISIBLE`?

* **你能创建自定义自定义视图吗？如何自定义？** Can you a create custom view? How?

* **什么是 `ViewGroup` 以及它们与 `View` 有何不同？** What are ViewGroups and how they are different from the Views?
    - `View`: 视图对象是 Android 中用户界面 (UI) 元素的基本构建块。视图是一个响应用户操作的简单矩形框。例如EditText、Button、CheckBox等。View是指android.view.View类，它是所有UI类的基类。View objects are the basic building blocks of User Interface(UI) elements in Android. View is a simple rectangle box which responds to the user’s actions. Examples are EditText, Button, CheckBox etc. View refers to the android.view.View class, which is the base class of all UI classes.

    - `ViewGroup`: ViewGroup是不可见的容器。它拥有 View 和 ViewGroup。例如，LinearLayout 是包含 Button(View) 的 ViewGroup，其他 Layouts 也是如此。ViewGroup 是布局的基类。ViewGroup is the invisible container. It holds View and ViewGroup. For example, LinearLayout is the ViewGroup that contains Button(View), and other Layouts also. ViewGroup is the base class for Layouts.

* **什么是画布`Canvas`？** What is a Canvas?

* **什么是`SurfaceView`？** - [英文资料](https://developer.android.com/reference/android/view/SurfaceView)  What is a `SurfaceView`?

* **相对布局与线性布局。** Relative Layout vs Linear Layout.

* **讲述约束布局**  Tell about Constraint Layout

* **你知道什么是视图树吗？你如何优化它的深度？** - [英文资料](https://developer.android.com/reference/android/view/ViewTreeObserver) Do you know what is the view tree? How can you optimize its depth?

* **Touch Control 和 Events 在 Android 中如何工作？** How does the Touch Control and Events work in Android?

<br>

---
<br>

#### Displaying Lists of Content 显示内容列表

* **`ListView` 和 `RecyclerView` 和有什么不一样？** - [英文资料](https://stackoverflow.com/questions/26728651/recyclerview-vs-listview) What is the difference between `ListView` and `RecyclerView`?

* **`RecyclerView` 内部是如何工作的？** How does RecyclerView work internally?

* **什么是`ViewHolder模式`？我们为什么要使用它？** - [英文资料](https://stackoverflow.com/questions/21501316/what-is-the-benefit-of-viewholder-pattern-in-android)  What is the ViewHolder pattern? Why should we use it?

* **RecyclerView优化-滚动性能提升** - [英文资料](https://amitshekhar.me/blog/recyclerview-optimization)RecyclerView Optimization - Scrolling Performance Improvement

* **`RecyclerView`优化嵌套** - [英文资料](https://amitshekhar.me/blog/setrecycledviewpool-for-optimizing-nested-recyclerview) Optimizing Nested RecyclerView

* **什么是`SnapHelper`？** - [SnapHelper](https://amitshekhar.me/blog/snaphelper)SnapHelper What is `SnapHelper`?


<br>

---
<br>

#### Dialogs and Toasts 对话和吐司

* **Android中的 `Dialog`有什么？** - [英文资料](https://developer.android.com/guide/topics/ui/dialogs)What is `Dialog` in Android?

* **Android中的 `Toast` 有什么？** - [英文资料](https://developer.android.com/guide/topics/ui/notifiers/toasts)  What is `Toast` in Android?

* **`Dialog`和`Dialog Fragment`之间有什么区别？** - [英文资料](https://stackoverflow.com/questions/7977392/android-dialogfragment-vs-dialog)  What the difference between `Dialog` and `Dialog Fragment`?
  
<br>

---
<br>

#### Intents and Broadcasting 意图和广播

* **什么是`Intent`？** What is `Intent`?

* **什么是隐式`Intent`？** What is an Implicit `Intent`?

* **什么是显式`Intent`？** What is an Explicit `Intent`?

* **什么是`BroadcastReceiver`？** - [英文资料](https://developer.android.com/guide/components/broadcasts)  What is a `BroadcastReceiver`?

* **什么是`LocalBroadcastManager`？** What is a `LocalBroadcastManager`?

* **`IntentFilter`的功能是什么？** - [英文资料](https://developer.android.com/reference/android/content/IntentFilter)  What is the function of an `IntentFilter`?

* **什么是粘性`Intent`？** What is a Sticky `Intent`?
    - 粘性 `Intents` 允许函数和服务之间的通信。`sendStickyBroadcast()` 执行称为粘性的 `sendBroadcast(Intent)`，即您发送的 Intent 在广播完成后仍然存在，以便其他人可以通过 registerReceiver(BroadcastReceiver, IntentFilter) 的返回值快速检索该数据。例如，如果您使用 ACTION_BATTERY_CHANGED 的意图来获取电池更换事件：当您为该操作调用 registerReceiver() 时——即使使用 null BroadcastReceiver——您将获得该操作的最后一次广播的 Intent。因此，您可以使用它来查找电池的状态，而不必注册电池中所有未来的状态变化。

  Sticky Intents allows communication between a function and a service. sendStickyBroadcast() performs a sendBroadcast(Intent) known as sticky, i.e. the Intent you are sending stays around after the broadcast is complete, so that others can quickly retrieve that data through the return value of registerReceiver(BroadcastReceiver, IntentFilter). For example, if you take an intent for ACTION_BATTERY_CHANGED to get battery change events: When you call registerReceiver() for that action — even with a null BroadcastReceiver — you get the Intent that was last Broadcast for that action. Hence, you can use this to find the state of the battery without necessarily registering for all future state changes in the battery.
    
* **描述广播broadcasts和意图intents如何工作，以便能够在您的应用程序周围传递消息？** - [英文资料](https://stackoverflow.com/questions/7276537/using-a-broadcast-intent-broadcast-receiver-to-send-messages-from-a-service-to-a) Describe how broadcasts and intents work to be able to pass messages around your app?

* **什么是`PendingIntent`？** What is a `PendingIntent`?
    - 如果你希望某人在未来某个时间点代表你执行任何 Intent 操作，那么我们将使用 Pending Intent。If you want someone to perform any Intent operation at future point of time on behalf of you, then we will use Pending Intent.
  

* **有哪些不同类型的广播Broadcasts？** - [英文资料](https://developer.android.com/guide/components/broadcasts) What are the different types of Broadcasts?

<br>

---
<br>

#### Services服务

* **什么是`Service`？** - [英文资料](https://developer.android.com/guide/components/services) What is `Service`?

* **`Service`对比`IntentService`** `Service` vs `IntentService`.

* **什么是`JobScheduler`？** - [英文资料](https://developer.android.com/reference/android/app/job/JobScheduler)   What is a `JobScheduler`?

<br>

---
<br>

#### Inter-process Communication 进程间通信

* **两个截然不同的 Android 应用程序如何交互？** - [英文资料](https://developer.android.com/training/basics/intents)   How can two distinct Android apps interact?

* **是否可以在多个进程中运行 Android 应用程序？如何？** - [英文资料](https://stackoverflow.com/questions/6567768/how-can-an-android-application-have-more-than-one-process)  Is it possible to run an Android app in multiple processes? How?

* **什么是 AIDL？列举通过 AIDL 创建有界服务的步骤** - [英文资料](https://developer.android.com/guide/components/aidl) What is AIDL? Enumerate the steps in creating a bounded service through AIDL.

* **您可以在 Android 中使用什么进行后台处理？** - [英文资料](https://developer.android.com/guide/background)  What can you use for background processing in Android?

* **什么是`ContentProvider`，它通常用于什么？** - [英文资料](https://developer.android.com/guide/topics/providers/content-provider-basics) and [here](https://developer.android.com/guide/topics/providers/content-providers) What is a `ContentProvider` and what is it typically used for?

<br>

---
<br>

#### Long-running Operations 长时间运行的操作

* **如何在 Java 或 Android 中并行运行任务，并在全部完成时获得回调？-与 Kotlin Flow 并行的长时间运行的任务** - [Long-running tasks in parallel with Kotlin Flow](https://amitshekhar.me/blog/long-running-tasks-in-parallel-with-kotlin-flow) How to run parallel tasks in Java or Android, and get callback when all complete?

* **为什么要避免在主线程上运行非 ui 代码？** - [英文资料](https://developer.android.com/training/multiple-threads/communicate-ui)  Why should you avoid to run non-ui code on the main thread?

* **什么是 ANR？如何预防 ANR？** - [英文资料](https://developer.android.com/topic/performance/vitals/anr.html)  What is ANR? How can the ANR be prevented?

* **什么是`AsyncTask`（在 API 级别 30 中弃用）？** What is an `AsyncTask`(Deprecated in API level 30) ?

* **`AsyncTask` 有什么问题？** What are the problems in AsyncTask?

* **您什么时候会使用 java 线程而不是 AsyncTask？** - [英文资料](https://stackoverflow.com/questions/18480206/asynctask-vs-thread-in-android)  When would you use java thread instead of an AsyncTask?

* **什么是`Loader`？（已弃用）** - [英文资料](https://developer.android.com/guide/components/loaders)  What is a `Loader`? (Deprecated)

* **`AsyncTask`和`Activity`的生命周期有什么关系？这会导致什么问题？如何避免这些问题？** What is the relationship between the life cycle of an `AsyncTask` and an `Activity`? What problems can this result in? How can these problems be avoided?
    - `AsyncTask` 与包含它的 `Activity` 的生命周期无关。因此，例如，如果您在 Activity 中启动 AsyncTask 并且用户旋转设备，则 Activity 将被销毁（并且将创建一个新的 Activity 实例）但 AsyncTask 不会死亡，而是继续存在直到它完成。
      An AsyncTask is not tied to the life cycle of the Activity that contains it. So, for example, if you start an AsyncTask inside an Activity and the user rotates the device, the Activity will be destroyed (and a new Activity instance will be created) but the AsyncTask will not die but instead goes on living until it completes.

    - 然后，当 `AsyncTask` 确实完成时，它不会更新新 `Activity` 的 UI，而是更新 `Activity` 的前一个实例（即创建它但不再显示的实例！）。这可能会导致异常（类型为 java.lang.IllegalArgumentException：如果您使用 findViewById 来检索 Activity 内的视图，则视图未附加到窗口管理器）。
      Then, when the AsyncTask does complete, rather than updating the UI of the new Activity, it updates the former instance of the Activity (i.e., the one in which it was created but that is not displayed anymore!). This can lead to an Exception (of the type java.lang.IllegalArgumentException: View not attached to window manager if you use, for instance, findViewById to retrieve a view inside the Activity).

    - 这也有可能导致内存泄漏，因为 AsyncTask 维护对 Activity 的引用，只要 AsyncTask 保持活动状态，就会阻止 Activity 被垃圾回收。。
      There’s also the potential for this to result in a memory leak since the AsyncTask maintains a reference to the Activity, which prevents the Activity from being garbage collected as long as the AsyncTask remains alive.

    - 由于这些原因，将 AsyncTasks 用于长时间运行的后台任务通常不是一个好主意。相反，对于长时间运行的后台任务，应该采用不同的机制（例如服务）。For these reasons, using AsyncTasks for long-running background tasks is generally a bad idea . Rather, for long-running background tasks, a different mechanism (such as a service) should be employed.
  
    - 注意：默认情况下，AsyncTasks 使用串行执行器在单个线程上运行，这意味着它只有 1 个线程，并且每个任务一个接一个地运行。Note: AsyncTasks by default run on a single thread using a serial executor, meaning it has only 1 thread and each task runs one after the other.
  

* **解释`Looper`,`Handler`和`HandlerThread`** Explain `Looper`, `Handler` and `HandlerThread`.

* **Android 内存泄漏和垃圾收集** Android Memory Leak and Garbage Collection

<br>

---
<br>

#### Working With Multimedia Content 处理多媒体内容

* **你如何处理 Android 中的位图，因为它占用太多内存？** - [英文资料](https://developer.android.com/topic/performance/graphics/load-bitmap) and [here](https://developer.android.com/topic/performance/graphics/manage-memory) How do you handle bitmaps in Android as it takes too much memory?

* **Bitmap常规图像和九补丁图像有什么区别？** What is the difference between a regular `Bitmap` and a nine-patch image?
    -通常，九补丁图像允许调整大小，可用作目标设备的背景或其他图像大小要求。九补丁指的是可以调整图像大小的方式：4 个角未缩放，4 个边缘在 1 个轴上缩放，中间一个可以缩放到两个轴。 In general, a Nine-patch image allows resizing that can be used as background or other image size requirements for the target device. The Nine-patch refers to the way you can resize the image: 4 corners that are unscaled, 4 edges that are scaled in 1 axis, and the middle one that can be scaled into both axes.
  

* **说说`Bitmap`池** - [英文资料](https://amitshekhar.me/blog/bitmap-pool) Tell about the `Bitmap` pool.

* **图像压缩是如何进行的？** How image compression is preformed?

<br>

---
<br>

#### Data Saving 数据保存

* **如何在 Android 应用程序中持久保存数据？** How to persist data in an Android app?

* **什么是 ORM？它是如何工作的？** What is ORM? How does it work?

* **你将如何`Activity`在屏幕旋转期间保持状态？** - [英文资料](https://stackoverflow.com/questions/3915952/how-to-save-state-during-orientation-change-in-android-if-the-state-is-made-of-m) How would you preserve `Activity` state during a screen rotation?

* **在 Android 应用程序中存储数据有哪些不同的方式？** What are different ways to store data in your Android app?

* **解释 Android 中的范围存储** Explain Scoped Storage in Android.

* **如何在 Android 中加密数据？** How to encrypt data in Android?

* **`SharedPreferences` 中的 `commit()` 和 `apply()` 是什么？** What is commit() and apply() in SharedPreferences?
    - `commit()` 通过同步写入数据，立即返回成功或失败的布尔值。 commit() returns a boolean value of success or failure immediately by writing data synchronously.
    - `apply()` 是异步的，它不会返回任何布尔响应。如果您有未完成的 apply() 并且您正在执行 commit()，那么 commit() 将被阻止，直到 apply() 未完成。apply() is asynchronous and it won't return any boolean response. If you have an apply() outstanding and you are performing commit(), then the commit() will be blocked until the apply() is not completed.

<br>

---
<br>

#### Look and Feel 外观和感觉

* **什么是`Spannable`？** What is a `Spannable`?

* **什么是`SpannableString`？** What is a `SpannableString`?
    - `SpannableString` 具有不可变的文本，但其跨度信息是可变的。当您的文本不需要更改但样式需要更改时，请使用 SpannableString。跨度是文本的范围，包括颜色、高度、斜体、链接等样式信息。A SpannableString has immutable text, but its span information is mutable. Use a SpannableString when your text doesn't need to be changed but the styling does. Spans are ranges over the text that include styling information like color, heighliting, italics, links, etc

* **在 Android 中使用文本的最佳做法什么是？** What are the best practices for using text in Android?

* **如何在任何应用程序中实现暗模式？** How to implement Dark mode in any application?

* **如何根据图像生成动态颜色？** How to generate dynamic colors based in image?

* **解释密度独立像素**  Explain about Density Independence Pixel

<br>

---
<br>

#### Memory Optimizations 内存优化

* **方法什么是`onTrimMemory()`？** - [英文资料](https://developer.android.com/topic/performance/memory) What is the `onTrimMemory()` method?

* **OutOfMemory 是如何发生的？** How does the OutOfMemory happens?

* **您如何发现 Android 应用程序中的内存泄漏？** How do you find memory leaks in Android applications?

<br>

---
<br>

#### Battery Life Optimizations 电池寿命优化

* **如何减少Android应用程序中的电池使用量？** How to reduce battery usage in an android application?

* **什么是Doze瞌睡？应用待机怎么样？** - [英文资料](https://developer.android.com/training/monitoring-device-state/doze-standby)  What is Doze? What about App Standby?

* **什么是`overdraw`？** - [英文资料](https://developer.android.com/topic/performance/rendering/overdraw.html)  What is `overdraw`?

<br>

---
<br>

#### Supporting Different Screen Sizes 支持不同的屏幕尺寸

* **您如何支持不同类型的决议？** - [英文资料](https://developer.android.com/training/multiscreen/screensizes)  How do you support different types of resolutions?

<br>

---
<br>

#### Permissions 权限

* **权限有哪些不同的保护级别？** What are the different protection levels in permission?

<br>

---
<br>

#### Native Programming 本机编程

* **什么是 NDK，它为什么有用？** - 英文资料: [Android NDK and RenderScript](https://amitshekhar.me/blog/ndk-and-renderscript)  What is the NDK and why is it useful?

* **什么是渲染脚本？**[Android NDK and RenderScript](https://amitshekhar.me/blog/ndk-and-renderscript)  What is renderscript?

<br>

---
<br>

#### Android System Internal 安卓系统内部

* **什么是安卓运行时？** - [Android Runtime](https://amitshekhar.me/blog/dalvik-art-jit-aot) What is Android Runtime?

* **Android 中的 Dalvik、ART、JIT 和 AOT** - [Dalvik, ART, JIT, and AOT](https://amitshekhar.me/blog/dalvik-art-jit-aot) Dalvik、ART、JIT 和 AOT   Dalvik, ART, JIT, and AOT in Android

* **Dalvik 和 ART 有什么区别** - [Difference between Dalvik and ART](https://amitshekhar.me/blog/dalvik-art-jit-aot) What are the differences between Dalvik and ART?

* **什么是DEX** - [英文资料](https://developer.android.com/reference/dalvik/system/DexFile)  What is DEX?

* **你能手动调用垃圾收集器吗？** - [是否可以在 Android 中强制垃圾收集？](https://www.youtube.com/watch?v=fPEjpFKo1-Q) Can you manually call the Garbage collector?

<br>

---
<br>

#### Android Jetpack 安卓喷气背包

* **什么是 `Android Jetpack` 以及为什么要使用它？** What is Android Jetpack and why to use this?

* **什么是 Android 架构组件？**  What are Android Architecture Components?

* **Android 中的 `LiveData` 什么是？** What is LiveData in Android?

* **`LiveData` 与 `ObservableField` 有何不同？**  How LiveData is different from ObservableField?

* **`LiveData` 中的 `setValue` 和 `postValue` 有什么区别？**  What is the difference between setValue and postValue in LiveData?

* **如何在 Android `Fragment`之间共享 `ViewModel`？**  How to share ViewModel between Fragments in Android?

* **解释 Android 中的工作管理器**  Explain Work Manager in Android.

* **Android 中 `WorkManager` 的用例** Use-cases of WorkManager in Android.

* **`ViewModel` 如何在内部工作？** How ViewModel work internally?

<br>

---
<br>

#### Others 其他的

* **为什么要使用`Bundle`类来传递数据，为什么我们不能使用简单的Map数据结构？** - [英文资料](https://developer.android.com/guide/components/activities/parcelables-and-bundles) Why Bundle class is used for data passing and why cannot we use simple Map data structure?

* **您如何对崩溃的应用程序进行故障排除？** - [英文资料](https://developer.android.com/topic/performance/vitals/crash)  How do you troubleshoot a crashing application?

* **解释Android通知系统？** Explain Android notification system?

* **Serializable 和 Parcelable 有什么区别？哪个是 Android 中最好的方法？** What is the difference between Serializable and Parcelable? Which is the best approach in Android?

* **什么是AAPT？** - [英文资料](https://developer.android.com/studio/command-line/aapt2)  What is AAPT?

* **定期更新屏幕的最佳方法什么是？** - [英文资料](https://stackoverflow.com/questions/5452394/best-way-to-perform-an-action-periodically-while-an-app-is-running-handler) What is the best way to update the screen periodically?

* **`FlatBuffers` 与 `JSON`** FlatBuffers vs JSON.

* **`HashMap`, `ArrayMap` and `SparseArray`**

* **什么是注解？**  What are Annotations?

* **如何创建自定义注释？** How to create custom Annotation?

* **如何在android中处理多点触控？** How to handle multi-touch in android?

* **什么是支持库？为什么介绍它？** What is the support library? Why was it introduced?

* **什么是安卓数据绑定？** What is Android Data Binding?

* **如何检查软件键盘是否可见？** How to check if Software keyboard is visible or not?

* **如何以编程方式在 Android 中截取屏幕截图？** How to take screenshot in Android programmatically?

<br>

---
<br>

### 三.Android Libraries 安卓库

 安卓面试题:

* **详解OkHttp拦截器——从这里学习** - [英文资料](https://amitshekhar.me/blog/okhttp-interceptor)Explain OkHttp Interceptor

* **OkHttp - HTTP 缓存** [英文资料](https://amitshekhar.me/blog/caching-with-okhttp-interceptor-and-retrofit) OkHttp - HTTP Caching

* **告诉我一些关于 RxJava 的事情** Tell me something about RxJava.

* **你将如何处理 RxJava 中的错误？** How will you handle error in RxJava?

* **`FlatMap` 与 `Map` 操作符** - [英文资料](https://amitshekhar.me/blog/rxjava-map-vs-flatmap)  FlatMap Vs Map Operator

* **`RxJava`什么时候用`Create`、`fromCallable`运算符，什么时候用运算符？** - [RxJava Create and fromCallable Operator](https://amitshekhar.me/blog/rxjava-create-and-fromcallable-operator) RxJava Create and fromCallable Operator When to use `Create` operator and when to use `fromCallable` operator of RxJava?

* **什么时候使用 RxJava 的 `defer` 运算符？** [defer 运算符](https://amitshekhar.me/blog/rxjava-defer-operator) RxJava Defer Operator  When to use `defer` operator of RxJava?

* **RxJava 中如何使用 `Timer`、`Delay` 和 `Interval` 运算符？** - [英文资料](https://amitshekhar.me/blog/rxjava-interval-operator) How are Timer, Delay, and Interval operators used in RxJava?

* **如何使用 RxJava 并行进行两个网络调用？** - [RxJava Zip Operator](https://amitshekhar.me/blog/rxjava-zip-operator) How to make two network calls in parallel using RxJava?
 
* **说出 `Concat` 和 `Merge` 的区别。** - [英文资料](https://amitshekhar.me/blog/rxjava-concat-operator) and [here](https://amitshekhar.me/blog/rxjava-merge-operator) Tell the difference between Concat and Merge.

* **在 `RxJava` 中解释主题？** - [英文资料](https://amitshekhar.me/blog/rxjava-subject-publish-replay-behavior-async)  Explain Subject in RxJava?

* **`RxJava` 中的 `Observable` 有哪些类型？** [Types Of Observables In RxJava](https://amitshekhar.me/blog/types-of-observables-in-rxjava)Types Observables In RxJava What are the types of Observables in RxJava?

* **如何在您的应用程序中使用 RxJava 实现搜索功能？** - 英文资料: [使用 RxJava 运算符进行即时搜索](https://amitshekhar.me/blog/instant-search-using-rxjava-operators)How to implement search feature using RxJava in your application?

* **使用 RxJava 运算符在 RecyclerView 中分页** - [英文资料](https://amitshekhar.me/blog/pagination-in-recyclerview-using-rxjava-operators) Pagination In RecyclerView Using RxJava Operators

* **Android 图片加载库 `Glide` 和 `Fresco` 是如何工作的？** - [英文资料](https://amitshekhar.me/blog/android-image-loading-library-optimize-memory-usage), [英文资料](https://amitshekhar.me/blog/android-image-loading-library-use-bitmap-pool-for-responsive-ui) and [英文资料](https://amitshekhar.me/blog/android-image-loading-library-solve-the-slow-loading-issue) How The Android Image Loading Library Glide and Fresco Works?

* **RxJava 中 `Schedulers.io()` 和 `Schedulers.computation()` 的区别。** Difference between Schedulers.io() and Schedulers.computation() in RxJava.

* **为什么我们在Android中使用像`Dagger`这样的依赖注入框架？** Why do we use the Dependency Injection Framework like Dagger in Android?

* **匕首`Dagger`如何工作？** How does the Dagger work?

* **`Dagger` 中的组件什么是？** What is Component in Dagger?

* **`Dagger` 中的模块什么是？** What is Module in Dagger?

* **自定义范围在 `Dagger` 中如何工作？** How does the custom scope work in Dagger?

* **什么时候在 `RxJava` 的 `CompositeDisposable` 上调用 `dispose` 和 `clear`？** - [英文资料](https://amitshekhar.me/blog/dispose-vs-clear-compositedisposable-rxjava) When to call dispose and clear on CompositeDisposable in RxJava?

* **什么是网络中的多部分请求？**  What is Multipart Request in Networking?

* **Kotlin 中的 `Flow` 什么是？** - [英文资料](https://amitshekhar.me/blog/flow-api-in-kotlin)   What is Flow in Kotlin?

<br>

---
<br>

### 四.Android Architecture 安卓架构

安卓面试题：

* **描述您上一个应用程序的架构** Describe the architecture of your last app.

* **描述`MVP`** Describe MVP.

* **描述 `MVVM`** - [MVVM Architecture](https://amitshekhar.me/blog/mvvm-architecture-android) MVVM架构 Describe MVVM.

* **`MVC` 与 `MVP` 与 `MVVM` 架构**  MVC vs MVP vs MVVM architecture.

* **什么是主持人presenter？** What is presenter?

* **什么是模型？** What is model?

* **描述 `MVC`** Describe MVC.

* **描述`MVI`**  Describe MVI

* **描述存储库模式**  Describe the repository pattern

* **什么是控制器？**  What is controller?

* **讲述一些关于干净代码的事情**  Tell something about clean code

<br>

---
<br>

### 五.Android Design Problem 安卓设计问题

安卓面试题：

* **设计优步应用程序** - [英文资料](https://github.com/amitshekhariitbhu/ridesharing-uber-lyft-app)   Design Uber App.

* **设计 Facebook 应用程序** Design Facebook App.

* **设计 Facebook Near-By Friends 应用程序** Design Facebook Near-By Friends App.

* **设计 WhatsApp** Design WhatsApp.

* **设计 SnapChat** Design SnapChat.

* **基于基于位置的应用程序的设计问题** Design problems based on location based app.

* **如何构建离线优先的应用程序？解释架构** How to build offline-first app? Explain the architecture.

* **设计 LRU 缓存** Design LRU Cache.

* **设计文件下载器** - [英文资料](https://github.com/amitshekhariitbhu/PRDownloader) Design File Downloader

* **设计图像加载库** - [英文资料](https://amitshekhar.me/blog/android-image-loading-library-optimize-memory-usage), [here](https://amitshekhar.me/blog/android-image-loading-library-use-bitmap-pool-for-responsive-ui) and [here](https://amitshekhar.me/blog/android-image-loading-library-solve-the-slow-loading-issue) Design an Image Loading Library

* **HTTP 请求与 HTTP 长轮询与 WebSockets** - [Learn from blog](https://amitshekhar.me/blog/http-request-long-polling-websocket-sse) and [Video - HTTP 请求与 HTTP 长轮询与 WebSocket 与服务器发送事件](https://www.youtube.com/watch?v=8ksWRX4xV-s) HTTP Request vs HTTP Long-Polling vs WebSockets

* **语音和视频通话如何工作？** - [英文资料](https://amitshekhar.me/blog/voice-and-video-call) How do Voice And Video Call Work?

<br>

---
<br>

### 六.Android Unit Testing 安卓单元测试

 安卓面试题：

* **什么是浓缩咖啡`Espresso`？** - [英文资料](https://developer.android.com/training/testing/ui-testing/espresso-testing.html)   What is Espresso?

* **什么是 `Robolectric`？** - [英文资料](http://robolectric.org/)  What is Robolectric?

* **使用 `Robolectric` 有哪些缺点？** - [英文资料](https://stackoverflow.com/questions/18271474/robolectric-vs-android-test-framework)  What are the disadvantages of using Robolectric?

* **什么是 UI-Automator？** - [英文资料](https://developer.android.com/training/testing/ui-testing/uiautomator-testing.html)  What is UI-Automator?

* **解释单元测试** - [英文资料](https://developer.android.com/training/testing/unit-testing/local-unit-tests)   Explain unit test.

* **解释仪器化测试** - [英文资料](https://developer.android.com/training/testing/unit-testing/instrumented-unit-tests)  Explain instrumented test.

* **你做过单元测试或自动测试吗？** Have you done unit testing or automatic testing?

* **为什么使用 Mockito？** [英文资料](http://site.mockito.org/)   Why Mockito is used?

* **描述 JUnit 测试** - [英文资料](https://en.wikipedia.org/wiki/JUnit)   Describe JUnit test.

* **描述代码覆盖率** Describe code coverage.

<br>

---
<br>

### 七.Android Tools And Technologies 安卓工具和技术

安卓面试题：

* **什么是ADB？** - [英文资料](https://developer.android.com/studio/command-line/adb)   What is ADB?

* **什么是 DDMS，您可以用它做什么？** - [英文资料](https://developer.android.com/studio/profile/monitor)  What is DDMS and what can you do with it?

* **什么是严格模式？** [StrictMode](https://amitshekhar.me/blog/strictmode-in-android-development)StrictMode What is the StrictMode?

* **Lint 是什么？它是干什么用的？**  What is Lint? What is it used for?

* **Git**

* **Android 开发有用的工具** Android Development Useful Tools.

* **Firebase** - [英文资料](https://firebase.google.com/)

* **如何测量Android中的方法执行时间？** How to measure method execution time in Android?

* **您可以访问您的 SQLite 数据库进行调试吗？** - [英文资料](https://github.com/amitshekhariitbhu/Android-Debug-Database) Can you access your database of SQLite Database for debugging?

* **使用Proguard有哪些需要注意的地方？** What are things that we need to take care while using Proguard?

* **Android 中的 Multidex 什么是？** What is Multidex in Android?

* **如何使用 Android Studio 内存分析器？** How to use Android Studio Memory Profiler?

* **如何在您的应用中使用 Firebase 实时数据库？** How to use Firebase realtime database in your app?

* **什么是Gradle？** What is Gradle?

* **APK 大小缩减** APK Size Reduction.

* **如何加快 Gradle 构建速度？** How can you speed up the Gradle build?

* **关于 gradle 构建系统** About gradle build system.

* **关于 android 应用程序的多个 apk** About multiple apk for android application.

* **混淆器是做什么用的？** What is proguard used for?

* **什么是混淆？它是干什么用的？缩小化呢？** What is obfuscation? What is it used for? What about minification?

* **如何在不更新应用程序的情况下更改应用程序中的某些参数？** How to change some parameters in an app without app update?

<br>

---
<br>

### 八.Java 和 Kotlin


#### OOP面向对象

* **解释 OOP 概念** Explain OOP Concepts.
    - 面向对象编程是一种使用类、对象、继承、多态、抽象和封装来设计程序的方法。Object-Oriented Programming is a methodology of designing a program using classes, objects,
      [inheritance](https://en.wikipedia.org/wiki/Inheritance_(object-oriented_programming)),
      [polymorphism](https://en.wikipedia.org/wiki/Polymorphism_(computer_science)),
      [abstraction](https://en.wikipedia.org/wiki/Abstraction_(software_engineering)), 和
      [encapsulation](https://en.wikipedia.org/wiki/Encapsulation_(computer_programming)).

* **构造函数和方法有什么区别？** What is the difference between a constructor and a method?
    - 构造函数的名称与类名相同，而方法的名称可以是任何名称。The name of the constructor is same as that of the class name, whereas the name of the method can be anything.
    - 构造函数没有返回类型。There is no return type of a constructor.
    - 当你创建一个类的对象时，该类的构造函数将被自动调用。但是对于方法，我们需要明确地调用它。When you make an object of a class, then the constructor of that class will be called automatically.
      But for methods, we need to call it explicitely.
    -构造函数不能被继承，但是可以通过调用 调用父类的构造函数super()。 Constructors can't be inherited but you can call the constructor of the parent class by calling `super()`.
    - 构造函数和方法它们都运行一段代码，但区别在于调用它们。Constructor and a method they both run a block of code but the difference is in calling them.
    - 我们可以直接使用他们的名字来调用方法。We can call method directly using their name.
    - 构造函数语法 Constructor Syntax 
        ```java
        public class SomeClassName{
            SomeClassName(parameter_list){ 
                ...
            } 
            ...
        }
        ```
    - 注意：在上面的语法中，构造函数的名称与类的名称相同，并且没有返回类型。
      Note:
      In the above syntax, the name of the constructor is the same as that of class
      and it has no return type.

    - 方法语法 Method Syntax
        ```java
        public class SomeClassName{
            public void someMethodName(parameter_list){
                ...
            }
            // call method
            someMethodName(parameter_list)
        }
        ```
* **抽象类和接口的区别？** Differences between abstract classes and interfaces?
    - 抽象类是包含具体方法和抽象方法（没有实现的方法）的类。抽象方法必须由抽象类的子类实现。抽象类不能被实例化，需要扩展才能使用。An abstract class, is a class that contains both concrete and abstract methods
      (methods without implementations). An abstract method must be implemented by the abstract class
      sub-classes. Abstract classes cannot be instantiated and need to be extended to be used.
    - 一个接口就像一个类的蓝图/契约（或者它可以被认为是一个有方法但没有它们的实现的类）。它包含表示其所有子类应具有的共同点的空方法。子类为这些方法中的每一个提供实现。接口已实现。An interface is like a blueprint/contract of a class (or it may be thought of as a class with methods, but without their implementation). It contains empty methods that
      represent, what all of its subclasses should have in common. The subclasses provide the
      implementation for each of these methods. Interfaces are implemented.

* **java中的迭代器和枚举有什么区别？** What is the difference between iterator and enumeration in java?
    - 在 Enumeration 中我们没有 remove() 方法，我们只能读取和遍历一个集合。In Enumeration we don't have remove() method and we can only read and traverse through a collection.
    - 迭代器可以应用于任何集合。在 Iterator 中，我们可以从集合中读取和删除项目。Iterators can be applied to any collection. In Iterator, we can read and remove items from a collection.

* **你同意我们使用组合而不是继承吗？** Do you agree we use composition over inheritance?

* **方法重载和覆盖之间的区别** Difference between method overloading and overriding.
  <p align="center">
  <img alt="重载和覆盖 Overloading and Overriding" src="https://github.com/youngWM/android-interview-questions-CN/blob/master/assets/overloading-vs-overriding.png">
  </p>
  
  - 重载发生在编译时，而覆盖发生在运行时：重载方法调用与其定义的绑定发生在编译时，而重载方法调用与其定义的绑定发生在运行时。有关静态与动态绑定的更多信息：StackOverflow。Overloading happens at compile-time while Overriding happens at runtime: The binding of overloaded method call to its definition happens at compile-time however binding of overridden method call to its definition happens at runtime.
      More info on static vs. dynamic binding: [StackOverflow](https://stackoverflow.com/questions/19017258/static-vs-dynamic-binding-in-java).
  
  - 静态方法可以被重载，这意味着一个类可以有多个同名的静态方法。静态方法不能被覆盖，即使您在子类中声明了相同的静态方法，它也与父类的相同方法无关，因为被覆盖的静态方法是由引用类选择的，而不是由对象的类选择的。Static methods can be overloaded which means a class can have more than one static method of same name. Static methods cannot be overridden, even if you declare a same static method in child class it has nothing to do with the same method of parent class as overridden static methods are chosen by the reference class and not by the class of the object.

  所以，例如：

```java
        public class Animal {
            public static void testClassMethod() {
                System.out.println("The static method in Animal");
            }

            public void testInstanceMethod() {
                System.out.println("The instance method in Animal");
            }
        }

        public class Cat extends Animal {
            public static void testClassMethod() {
                System.out.println("The static method in Cat");
            }

            public void testInstanceMethod() {
                System.out.println("The instance method in Cat");
            }

            public static void main(String[] args) {
                Cat myCat = new Cat();
                myCat.testClassMethod();
                Animal myAnimal = myCat;
                myAnimal.testClassMethod();
                myAnimal.testInstanceMethod();
            }
        }
```

将输出：

```java
        The static method in Cat    // testClassMethod() is called from "Cat" reference

        The static method in Animal // testClassMethod() is called from "Animal" reference,
                                    // ignoring actual object inside it (Cat)

        The instance method in Cat  // testInstanceMethod() is called from "Animal" reference,
                                    // but from "Cat" object underneath
```

- 最基本的区别是重载是在同一个类中完成的，而重写基类和子类是必需的。重写就是对父类继承的方法进行具体的实现。The most basic difference is that overloading is being done in the same class while for overriding base and child classes are required. Overriding is all about giving a specific implementation to the inherited method of parent class.

- 静态绑定用于重载方法，动态绑定用于覆盖/覆盖方法。性能：与覆盖相比，重载提供更好的性能。原因是重写方法的绑定是在运行时完成的。Static binding is being used for overloaded methods and dynamic binding is being used for overridden/overriding methods.
      Performance: Overloading gives better performance compared to overriding. The reason is that the binding of overridden methods is being done at runtime.

- private 和 final 方法可以重载，但不能被覆盖。这意味着一个类可以有多个同名的私有/最终方法，但子类不能覆盖其基类的私有/最终方法。Private and final methods can be overloaded but they cannot be overridden. It means a class can have more than one private/final methods of same name but a child class cannot override the private/final methods of their base class.

- 在方法重载的情况下，方法的返回类型无关紧要，可以相同也可以不同。然而，在方法覆盖的情况下，覆盖方法可以有更具体的返回类型（意味着，例如，如果基方法返回 Number 类的实例，所有覆盖方法可以返回从 Number 扩展的任何类，但不是在层次结构中更高，例如，对象在这种特殊情况下）。Return type of method does not matter in case of method overloading, it can be same or different. However in case of method overriding the overriding method can have more specific return type (meaning if, for example, base method returns an instance of Number class, all overriding methods can return any class that is extended from Number, but not a class that is higher in the hierarchy, like, for example, Object is in this particular case).

- 进行方法重载时参数列表应该不同。方法重写中的参数列表应该相同。注释重写的方法也是一个好习惯，这样@Override编译器就可以在子类确实在编译时重写父类的类方法时通知您。Argument list should be different while doing method overloading. Argument list should be same in method Overriding.
      It is also a good practice to annotate overridden methods with `@Override` to make the compiler be able to notify you if child is, indeed, overriding parent's class method during compile-time.

* **您知道哪些访问修饰符？每个做什么？** What are the access modifiers you know? What does each one do?<br>
    - Java 语言中有四种访问修饰符（从最严格到最宽松）：There are four access modifiers in Java language (from strictest to the most lenient):
        1. `private` 变量、方法、构造函数或内部类仅对其包含的类及其方法可见。此修饰符最常用，例如，仅允许通过 getter 和 setter 访问变量，或隐藏用户不应使用的类的底层实现，从而保持封装。还标记了单例构造函数private以避免从外部进行不需要的实例化。`private` *variables*, *methods*, *constructors* or *inner classes* are only visible to its' containing class and its' methods. This modifier is most commonly used, for example, to allow variable access only through getters and setters or to hide underlying implementation of classes that should not be used by user and therefore maintain encapsulation. Singleton constructor is also marked `private` to avoid unwanted instantiation from outside.
        2. `Default`（不使用关键字）此修饰符可应用于类、变量、构造函数和方法，并允许从同一包内的类和方法进行访问。`Default` (no keyword is used) this modifier can be applied to *classes*, *variables*, *constructors* and *methods* and allows access from classes and methods inside the same package.
        3. `protected`可用于变量、方法和构造函数，因此只允许访问与受保护成员的类位于同一包内的子类和类。`protected` can be used on *variables*, *methods* and *constructors* therefore allowing access only to subclasses and classes that are inside the same package as protected members' class.
        4.`public`修饰符广泛用于类、变量、构造函数和方法，以授予从任何地方的任何类和方法的访问权限。它不应该在任何地方使用，因为它意味着标记为public不敏感的数据并且不能用于损害程序。 `public` modifier is widely-used on *classes*, *variables*, *constructors* and *methods* to grant access from any class and method anywhere. It should not be used everywhere as it implies that data marked with `public` is not sensitive and can not be used to harm the program.

* **一个接口可以实现另一个接口吗？** Can an Interface implement another Interface?
    - 是的，一个接口可以实现另一个接口（并且不止一个），但是它需要使用extends, 而不是implements关键字。虽然您不能从父接口中删除方法，但您可以向子接口自由添加新方法。Yes, an interface can implement another interface (and more than one), but it needs to use `extends`, rather than `implements` keyword. And while you can not remove methods from parent interface, you can add new ones freely to your sub-interface.

* **什么是多态？什么是继承？** What is Polymorphism? What about Inheritance?
    - Java中的多态有两种类型：编译时多态（静态绑定）和运行时多态（动态绑定）。方法重载是静态多态的一个例子，而方法覆盖是动态多态的一个例子。Polymorphism in Java has two types: Compile time polymorphism (static binding) and Runtime polymorphism (dynamic binding). Method overloading is an example of static polymorphism, while method overriding is an example of dynamic polymorphism.

      多态性的一个重要示例是父类如何引用子类对象。事实上，任何满足多个 IS-A 关系的对象在本质上都是多态的。An important example of polymorphism is how a parent class refers to a child class object.  In fact, any object that satisfies more than one IS-A relationship is polymorphic in nature.

      例如，让我们考虑一个类Animal，让Cat成为 的子类Animal。所以，任何猫都是动物。在这里，Cat 满足其自身类型及其超类 Animal 的 IS-A 关系。For instance, let’s consider a class `Animal` and let `Cat` be a subclass of `Animal`. So, any cat IS animal. Here, Cat satisfies the IS-A relationship for its own type as well as its super class Animal.
    - 继承可以定义为一个类获取另一个类的属性（方法和字段）的过程。通过使用继承，可以按层次顺序管理信息。Inheritance can be defined as the process where one class acquires the properties (methods and fields) of another. With the use of inheritance the information is made manageable in a hierarchical order.

      继承其他属性的类称为子类（派生类、子类），继承属性的类称为超类（基类、父类）。The class which inherits the properties of other is known as subclass (derived class, child class) and the class whose properties are inherited is known as superclass (base class, parent class).

      继承使用关键字extends来继承类的属性。以下是 extends 关键字的语法。Inheritance uses the keyword `extends` to inherit the properties of a class. Following is the syntax of extends keyword.
      ```java
      class Super {
         .....
         .....
      }
      class Sub extends Super {
         .....
         .....
      }
      ```

* **java类和接口中的多重继承** Multiple inheritance in Classes and Interfaces in java

* **什么是设计模式？** What are the design patterns?
    - 创作模式 Creational patterns
        - 生成器 Builder [Wikipedia](https://en.wikipedia.org/wiki/Builder_pattern?oldformat=true)
        - 工厂 Factory [Wikipedia](https://en.wikipedia.org/wiki/Factory_method_pattern?oldformat=true)
        - 单例 Singleton [Wikipedia](https://en.wikipedia.org/wiki/Singleton_pattern)
        - 单州 Monostate [Wikipedia](http://wiki.c2.com/?MonostatePattern)
        - 流畅的界面模式 Fluent Interface Pattern [Wikipedia](https://martinfowler.com/bliki/FluentInterface.html)
    - 结构模式 Structural patterns
        - 适配器 Adapter [Wikipedia](https://en.wikipedia.org/wiki/Adapter_pattern?oldformat=true)
        - 装饰 Decorator [Wikipedia](https://en.wikipedia.org/wiki/Decorator_pattern?oldformat=true)
        - 外观 Facade [Wikipedia](https://en.wikipedia.org/wiki/Facade_pattern?oldformat=true)
    - 行为模式 Behavioural patterns
        - 责任链 Chain of responsibility [Wikipedia](https://en.wikipedia.org/wiki/Chain-of-responsibility_pattern?oldformat=true)
        - 迭代器 Iterator [Wikipedia](https://en.wikipedia.org/wiki/Iterator_pattern?oldformat=true)
        - 策略 Strategy [Wikipedia](https://en.wikipedia.org/wiki/Strategy_pattern?oldformat=true)

<br>

---
<br>

#### Collections and Generics 集合和泛型

* **数组与数组列表** - [英文资料](https://stackoverflow.com/questions/32020000/what-is-the-difference-between-an-array-arraylist-and-a-list/32020072) Arrays Vs ArrayLists

* **HashSet 与 TreeSet** - [英文资料](https://stackoverflow.com/questions/25602382/java-hashset-vs-treeset-when-should-i-use-over-other)   HashSet Vs TreeSet

* **HashMap 与 Set**[英文资料](https://stackoverflow.com/questions/2773824/difference-between-hashset-and-hashmap)    HashMap Vs Set

* **堆栈与队列** Stack Vs Queue

* **解释 Java 中的泛型？** Explain Generics in Java?
    - 泛型包含在 Java 语言中以提供更强的类型检查，通过允许程序员定义哪些类可以与其他类一起使用。Generics were included in Java language to provide stronger type checks, by allowing the programmer to define, which classes can be used with other classes
      > 简而言之，泛型使类型（类和接口）在定义类、接口和方法时成为参数。与方法声明中使用的更熟悉的形式参数非常相似，类型参数为您提供了一种方法，可以通过不同的输入重复使用相同的代码。区别在于形式参数的输入是值，而类型参数的输入是类型。（官方 Java 文档）。In a nutshell, generics enable types (classes and interfaces) to be parameters when defining classes, interfaces and methods. Much like the more familiar formal parameters used in method declarations, type parameters provide a way for you to re-use the same code with different inputs. The difference is that the inputs to formal parameters are values, while the inputs to type parameters are types. ([Official Java Documentation](https://docs.oracle.com/javase/tutorial/java/generics/why.html))

    - 这意味着，例如，您可以定义：This means that, for example, you can define:
        ```java
        List<Integer> list = new ArrayList<>();
        ```
      并让编译器注意，如果您将某些类型以外的对象Integer放入此列表并警告您。And let the compiler take care of noticing, if you put some object, of type other than `Integer` into this list and warn you.
    - 应该注意的是，标准类层次结构不适用于泛型类型。这意味着IntegerinList<Integer>不是继承自<Number>- 它实际上是直接继承自<Object>. 您仍然可以通过使用,或 之类的通配符来限制哪些类可以作为参数传递给泛型。<?><? extends MyCustomClass><? super Number> 。    It should be noted that standard class hierarchy *does not* apply to generic types. It means that `Integer` in `List<Integer>` is not inherited from `<Number>` - it is actually inherited directly from `<Object>`. You can still put some constraints on what classes can be passed as a parameter into a generic by using [wildcards](https://docs.oracle.com/javase/tutorial/extra/generics/wildcards.html) like `<?>`, `<? extends MyCustomClass>` or `<? super Number>`.
    - 虽然泛型非常有用，但后来包含在 Java 语言中对它们的实现施加了一些限制——向后兼容性要求它们只保留“语法糖”——它们在编译时被擦除（类型擦除）并被类object替换。While generics are very useful, late inclusion into Java language has put some restraints on their implementation - backward compatibility required them to remain just "syntactic sugar" - they are erased ([type erasure](https://docs.oracle.com/javase/tutorial/java/generics/erasure.html)) during compile-time and replaced with `object` class.

* **什么是 Java 优先级队列？** What is Java PriorityQueue?
    - 在优先队列中，每个元素都有一定的优先级，所有元素都出现在一个队列中。这些操作是根据优先级执行的。In Priority Queue, each element is having some priority and all the elements are present in a queue. The operations are performed based on the priority.

<br>

---
<br>

#### Objects and Primitives 对象和基元

* **类是如何String实现的？为什么它是不可变的？** How is `String` class implemented? Why was it made immutable?
    - Java 语言中没有Stringclass 的原始变体 - 所有字符串都只是底层字符数组的包装器，它被声明为final. 这意味着，一旦一个String对象被实例化，它就不能通过语言的常规工具进行更改（反射仍然会把事情搞得一团糟，因为在 Java 中没有对象是真正不可变的）。这就是为什么String类中的变量是第一个要使用的候选者，当你想覆盖hashCode()你equals()的类时 - 你可以肯定，他们所有需要的合同都会得到满足。There is no primitive variant of `String` class in Java language - all strings are just wrappers around underlying array of characters, which is declared `final`. This means that, once a `String` object is instantiated, it cannot be changed through normal tools of the language (Reflection still can mess things up horribly, because in Java no object is truly immutable). This is why `String` variables in classes are the first candidates to be used, when you want to override `hashCode()` and `equals()` of your class - you can be sure, that all their required contracts will be satisfied.
      > 注意：String 类是不可变的，因此一旦创建，String 对象就不能更改。String 类有许多方法，其中一些将在下面讨论，它们似乎可以修改字符串。由于字符串是不可变的，这些方法真正做的是创建并返回一个包含操作结果的新字符串。（官方 Java 文档）Note: The String class is immutable, so that once it is created a String object cannot be changed. The String class  has a number of methods, some of which will be discussed below, that appear to modify strings. Since strings are  immutable, what these methods really do is create and return a new string that contains the result of the operation. ([Official Java Documentation](https://docs.oracle.com/javase/tutorial/java/data/strings.html))

      这个类在某种意义上也是独一无二的，当你创建一个这样的实例时。This class is also unique in a sense, that, when you create an instance like this:
      ```java
      String helloWorld = "Hello, World!";
      ```
      Hello, World!被称为文字String，编译器用它的值创建一个对象。所以 `"Hello, World!"` is called a *literal* and compiler creates a `String` object with its' value. So
      ```java
        String capital = "Hello, World!".toUpperCase();
      ```
      是一个有效的语句，它首先会创建一个字面值为“Hello, World!”的对象。然后将创建并返回另一个值为“HELLO, WORLD!”的对象   is a valid statement, that, firstly, will create an object with literal value "Hello, World!" and then will create and return another object with value "HELLO, WORLD!"
    - String是不可变的，以防止恶意操纵数据，例如，当用户登录或其他敏感数据被发送到服务器时。`String` was made immutable to prevent malicious manipulation of data, when, for example, user login or other sensitive data is being send to a server.

* **说String是不可变的什么是意思？What does it means to say that a `String` is immutable?**
    - 这意味着一旦创建，String对象char[]（它的包含值）就被声明final，因此在运行时不能更改。It means that once created, `String` object's `char[]` (its' containing value) is declared `final` and, therefore, it can not be changed during runtime.

* **什么是String.intern()？何时以及为什么应该使用它？What is `String.intern()`? When and why should it be used?**
    - String.intern()用于管理 Java 代码中的内存。当我们在不同的字符串中有重复值时使用它。当您调用 时String.intern()，如果在字符串池中存在该字符串，则该equals()方法将返回 true 并且仅返回该字符串。`String.intern()` is used to mange memory in Java code. It is used when we have duplicates value in different strings. When you call the `String.intern()`, then if in the String pool that string is present then the `equals()` method will return true and it will return that string only.

* **你能在 Java 中列出 8 种基本类型吗？ Can you list 8 primitive types in java?**
    - `byte`
    - `short`
    - `int`
    - `long`
    - `float`
    - `double`
    - `char`
    - `String`
    - `boolean`

* **整数和整数有什么区别？** What is the difference between an Integer and int?
    - int是原始数据类型 (with boolean, byte, char, short, long, floatand double)，而Integer(with Boolean, Byte, Character, Short, Long, Floatand Double) 是封装原始数据类型的包装类，同时提供有用的方法来执行不同的任务。 `int` is a primitive data type (with `boolean`, `byte`, `char`, `short`, `long`, `float` and `double`), while `Integer` (with `Boolean`, `Byte`, `Character`, `Short`,`Long`, `Float` and `Double`) is a [wrapper](https://docs.oracle.com/javase/tutorial/java/data/numberclasses.html) class that encapsulates primitive data type, while providing useful methods to perform different tasks with it.

* **什么是自动装箱和拆箱？** What is Autoboxing and Unboxing?
    - 自动装箱和拆箱是对具有“包装器”类的原始数据类型进行自动包装（放入盒子中）和展开（取出值）的过程。Soint和Integer可以（几乎总是）在 Java 语言中互换使用，这意味着方法既void giveMeInt(int i) { ... }可以作为参数int也可以作为Integer参数。 Autoboxing and Unboxing is the process of automatic wrapping (putting in a box) and unwrapping (getting the value out) of primitive data types, that have "wrapper" classes. So `int` and `Integer` can (almost always) be used interchangeably in Java language, meaning a method `void giveMeInt(int i) { ... }` can take `int` as well as `Integer` as a parameter.

* **Java 中的类型转换**  Typecast in Java
    - 在 Java 中，您可以使用强制转换将一个类变形为另一个兼容的类。例如：In Java, you can use casts to polymorph one class into another, compatible one. For example:
        ```java
            long i = 10l;
            int j = (int) i;
            long k = j;
        ```
      在这里我们看到，虽然缩小（long i-> int j）需要显式转换以确保程序员意识到，可能会有一些数据或精度损失，但加宽（int j-> long k）不需要显式转换，因为不可能数据丢失（long可以采用比int允许的更大的数字）。Here we see, that, while narrowing (`long i` -> `int j`) requires an explicit cast to make sure the programmer realizes, that there may be some data or precision loss, widening (`int j` -> `long k`) does not require an explicit cast, because there can be no data loss (`long` can take larger numbers than `int` allows).

* **对象在 Java 中是通过引用传递还是通过值传递？对此进行详细说明。 Do objects get passed by reference or value in Java? Elaborate on that.**
    - 在 Java 中，所有原语和对象都是按值传递的，这意味着它们的副本将在接收方法中进行操作。但有一点需要注意——当您将一个对象引用传递给一个方法时，会生成该引用的一个副本，因此它仍然指向同一个对象。这意味着，当方法退出时，您对该对象内部所做的任何更改都将保留。 In Java all primitives and objects are passed by value, meaning that their copy will be manipulated in the receiving method. But there is a caveat - when you pass an object reference into a method, a *copy of this reference* is made, so it still points to the same object. This means, that any changes that you make to the insides of this object are retained, when the method exits.
        ```java
        public class Pointer {

            int innerField;

            public Pointer(int a) {
                this.innerField = a;
            }
        }
        ```
        ```java
        public class ValueAndReference {

            public static void main(String[] args) {

                Pointer a = new Pointer(0);
                int b = 1;

                print("Before:");
                print("b = " + b);
                print("a.innerField = " + a.innerField);
                exampleMethod(a, b);
                print("After:");
                print("b = " + b);
                print("a.innerField = " + a.innerField);
            }

            static void exampleMethod(Pointer a, int b) {
                a.innerField = 2;
                b = 10;
            }

            static void print(String text) {
                System.out.println(text);
            }
        }
        ```
      将输出：
        ```java
            Before:

            b = 1

            a.innerField = 0

            After:

            b = 1        // a new local int variable was created and operated on, so "b" didn't change

            a.innerField = 2 // Pointer a got its' innerField variable changed
                             //  from 0 to 2, because method was operating on
                             //  the same reference to an instance
        ```

* **对象的实例化和初始化有什么区别？** What is the difference between instantiation and initialization of an object?

* **局部变量、实例变量和类变量之间有什么区别？** What the difference between local, instance and class variables?
    - 局部变量仅存在于创建它们的方法中，它们单独存储在各自的线程堆栈中（有关更多信息，请参阅有关 Java 内存模型的问题）并且不能将它们的引用传递到方法范围之外。这也意味着它们不能被分配任何访问修饰符或制作static- 因为它们只存在于封闭方法的执行期间并且这些修饰符没有意义，因为无论如何其他外部方法都无法获得它们。 Local variables exist only in methods that created them, they are stored separately in their respected Thread Stack (for more information, see question about Java Memory Model) and cannot have their reference passed outside of the method scope. That also means that they cannot be assigned any access modifier or made `static` - because they only exist during enclosing method's execution and those modifiers just do not make sense, since no other outside method can get them anyway.
    - 实例变量是那些在类中声明的变量，它们的值在类的一个实例和另一个实例之间可能不同，但它们始终需要该类的实例存在。Instance variables are the ones, that are declared in classes and their value can be different from one instance of the class to another, but they always require that class' instance to exist.
    - 类变量是那些static在类的主体中标有关键字的变量。它们在那个类的所有实例中只能有一个值（在一个地方改变它会在它们的类中改变它，因此在所有实例中）并且甚至可以在没有那个类的实例的情况下被检索（如果它们的访问修饰符允许的话） .Class variables are those, that are marked with `static` keyword in their class' body. They can only have one value across all instances of that class (changing it in one place will change it in their class and, therefore, in all instances) and can even be retrieved without that class' instance (if their access modifier allows it).

<br>

---
<br>

#### Java Memory Model and Garbage Collector Java 内存模型和垃圾收集器

* **什么是垃圾收集器？它是如何工作的？** What is garbage collector? How does it work?
    - 所有对象都分配在 JVM 管理的堆区域上。只要一个对象被引用，JVM 就认为它是活动的。一旦某个对象不再被引用，因此应用程序代码无法访问该对象，垃圾收集器就会将其删除并回收未使用的内存。All objects are allocated on the heap area managed by the JVM.
      As long as an object is being referenced, the JVM considers it alive.
      Once an object is no longer referenced and therefore is not reachable by the application code,
      the garbage collector removes it and reclaims the unused memory.

* **什么是 Java 内存模型？它保证哪些合同？它的堆和栈是如何组织的？** What is Java Memory Model? What contracts does it guarantee? How are its' Heap and Stack organized?

* **什么是内存泄漏以及 Java 如何处理它？** What is memory leak and how does Java handle it?

* **Java 中的强引用、软引用、弱引用和虚引用什么是？** What are strong, soft, weak and phantom references in Java?

<br>

---
<br>

#### Concurrency 并发

* **关键字什么是synchronized意思？** What does the keyword `synchronized` mean?

* **什么是ThreadPoolExecutor？** - [ThreadPoolExecutor in Android](https://amitshekhar.me/blog/threadpoolexecutor-in-android) Android 中的 ThreadPoolExecutor What is a `ThreadPoolExecutor`?

* **什么是volatile修饰符？**  What is `volatile` modifier?

* **原子包中的类公开了一组通用方法：get、set,、lazyset、compareAndSet和weakCompareAndSet。请描述它们。 The classes in the atomic package expose a common set of methods: `get`, `set,`, `lazyset`, `compareAndSet`, and `weakCompareAndSet`. Please describe them.**

<br>

---
<br>

#### Exceptions 例外情况

* **try{}, catch{},是如何finally工作的？**  How does the `try{}`, `catch{}`, `finally` works?

* **Checked Exceptiona和 an 和有什么不一样Un-Checked Exception？**  What is the difference between a `Checked Exception` and an `Un-Checked Exception`?

#### Others 其他的

* **什么是序列化？你如何实施它？**  What is serialization? How do you implement it?
    - 序列化是将对象转换为字节流以便将对象存储到内存中的过程，以便以后可以重新创建它，同时仍保持对象的原始状态和数据。在 Android 中，您可以使用 Serializable、Externalizable（实现 Serializable）或 Parcelable 接口。Serialization is the process of converting an object into a stream of bytes in order to store
      an object into memory, so that it can be recreated at a later time, while still keeping the
      object's original state and data. In Android you may use either the Serializable, Externalizable (implements Serializable) or Parcelable interfaces.
    - 虽然 Serializable 是最容易实现的，但如果您需要将自定义逻辑插入到序列化过程中，则可以使用 Externalizable（尽管现在几乎从未使用过，因为它被认为是 Java 早期版本的遗留物）。但强烈建议在 Android 中使用 Parcelable，因为 Parcelable 是专门为 Android 创建的，它的执行速度比 Serializable 快 10 倍左右，因为 Serializable 使用反射，这是一个缓慢的过程并且往往会创建很多临时对象并且它可能导致垃圾收集更频繁地发生。While Serializable is the easiest to implement, Externalizable may be used if you need to insert custom logic into the process of serialization (although it is almost never used nowadays as it is considered a relic from early versions of Java). But it is highly recommended to use Parcelable in Android instead, as Parcelable was created exclusively for Android and it performs about 10x faster than Serializable, because Serializable uses reflection, which is a slow process and tends to create a lot of temporary objects and it may cause garbage collection to occur more often.
    - 要使用 Serializable，您所要做的就是实现接口：To use Serializable all you have to do is implement the interface:
        ```java
        // Implementing the Serializable interface is all that is required
        public class User implements Serializable {

            private String name;
            private String email;

                public User() {
                }

                public String getName() {
                    return name;
                }

                public void setName(final String name) {
                    this.name = name;
                }

                public String getEmail() {
                    return email;
                }

                public void setEmail(final String email) {
                    this.email = email;
                }
            }
        ```
    - Parcelable requires a bit more work:
        ```java
            public class User implements Parcelable {

                private String name;
                private String email;

                /**
                 * Interface that must be implemented and provided as a public CREATOR field
                 * that generates instances of your Parcelable class from a Parcel.
                 */
                public static final Creator<User> CREATOR = new Creator<User>() {

                    /**
                     * Creates a new USer object from the Parcel. This is the reason why
                     * the constructor that takes a Parcel is needed.
                     */
                    @Override
                    public User createFromParcel(Parcel in) {
                        return new User(in);
                    }

                    /**
                     * Create a new array of the Parcelable class.
                     * @return an array of the Parcelable class,
                     * with every entry initialized to null.
                     */
                    @Override
                    public User[] newArray(int size) {
                        return new User[size];
                    }
                };

                public User() {
                }

                /**
                 * Parcel overloaded constructor required for
                 * Parcelable implementation used in the CREATOR
                 */
                private User(Parcel in) {
                    name = in.readString();
                    email = in.readString();
                }

                public String getName() {
                    return name;
                }

                public void setName(final String name) {
                    this.name = name;
                }

                public String getEmail() {
                    return email;
                }

                public void setEmail(final String email) {
                    this.email = email;
                }

                @Override
                public int describeContents() {
                    return 0;
                }

                /**
                 * This is where the parcel is performed.
                 */
                @Override
                public void writeToParcel(final Parcel parcel, final int i) {
                    parcel.writeString(name);
                    parcel.writeString(email);
                }
            }
        ```
      注意：有关describeContents()方法的完整说明，请参阅StackOverflow。在 Android Studio 中，您可以为您自动生成所有可打包代码，但与其他所有内容一样，尝试并理解正在发生的一切总是一件好事。Note: For a full explanation of the <b>describeContents()</b> method see [StackOverflow](https://stackoverflow.com/questions/4076946/parcelable-where-when-is-describecontents-used/4914799#4914799).
      In Android Studio, you can have all of the parcelable code auto generated for you, but like with everything else, it is always a good thing to try and understand everything that is happening.

* **什么是transient修饰符？**  What is `transient` modifier?

* **什么是匿名类？**  What are anonymous classes?

* **一个对象使用`==`和`.equals`有什么区别？**  What is the difference between using `==` and `.equals` on an object?

* **`hashCode()`和`equals()`是做什么用的？**  What is the `hashCode()` and `equals()` used for?

* **为什么不在构造函数中调用抽象方法？** - [英文资料](https://stackoverflow.com/questions/15327417/is-it-ok-to-call-abstract-method-from-constructor-in-java)   Why would you not call abstract method in constructor?

* **你什么时候会创建一个对象值final？**  When would you make an object value `final`?

* **final这些finally和关键字什么是finalize？**  What are these `final`, `finally` and `finalize` keywords?
    - final是java语言中的关键字。它用于对类、方法和变量应用限制。final 类不能继承，final 方法不能重写，final 变量值不能改变。 `final` is a keyword in the java language. It is used to apply restrictions on class, method and variable. Final class can't be inherited, final method can't be overridden and final variable value can't be changed.
      ```java
      class FinalExample {
          public static void main(String[] args) {
              final int x=100;
              x=200;//Compile Time Error because x is final
          }
      }
      ```
    - `finally` is a code block and is used to place important code, it will be executed whether exception is handled or not.
      ```java
      class FinallyExample {
          public static void main(String[] args) {
              try {
                  int x=300;
              }catch(Exception e) {
                  System.out.println(e.getMessage());            }
              finally {
                  System.out.println("finally block is executed");
              }
          }
      }
      ```
    - `Finalize` is a method used to perform clean up processing just before object is garbage collected.
      ```java
      class FinalizeExample {
          public void finalize() {
              System.out.println("finalize called");
          }
  
          public static void main(String[] args) {
              FinalizeExample f1=new FinalizeExample();
              FinalizeExample f2=new FinalizeExample();
              f1=null;
              f2=null;
              System.gc();
          }
      }
      ```

* **Java中的“throw”和“throws”关键字有什么区别？** What is the difference between "throw" and "throws" keyword in Java?
    - throws仅用于指示要抛出哪个异常。但是throw关键字用于从任何静态块或任何方法中抛出一些异常。`throws` is just used to indicated which exception is to be thrown. But the `throw` keyword is used to throw some exception from any static block or any method.

* **static这个词在Java中什么是意思？** What does the `static` word mean in Java?
    - 在变量的情况下static，这意味着该变量（它的值或它引用的对象）跨越封闭类的所有实例（在一个实例中更改它会影响所有其他实例），而在方法的情况下，这意味着可以调用这些static方法没有他们的封闭类的实例。它很有用，例如，当您创建不需要每次要使用它们时都实例化的实用程序类。In case of `static` variable it means that this variable (its' value or the object it references) spans across all instances of enclosing class (changing it in one instance affects all others), while in case of `static` methods it means that these methods can be invoked without an instance of their enclosing class. It is useful, for example, when you create util classes that need not be instantiated every time you want to use them.

* **static可以在 Java 中重写方法吗？** Can a `static` method be overridden in Java?
    - 虽然子类可以用另一个具有相同签名的静态方法覆盖静态方法（返回类型可以向下转换），但它并不是真正被覆盖 - 它变成了“隐藏”，但在正确的情况下仍然可以访问这两种方法（参见关于上面的重载/覆盖的问题）。While child class can override a static method with another static method with the same signature (return type can be down-casted), it is not truly overridden - it becomes "hidden", but both methods can still be accessed under right circumstances (see question about overloading/overriding above).

* **什么时候static运行块？** When is a `static` block run?
    - 静态块中的代码仅执行一次：第一次创建该类的对象或第一次访问该类的静态成员（即使您从未创建该类的对象）。Code inside static block is executed only once: the first time you make an object of that class or the first time you access a static member of that class (even if you never make an object of that class).

* **什么是反射？** What is reflection?
    - 您可以借助反射在运行时检查类、接口、字段和方法，最好的部分是您不需要知道这些类、方法等的名称。You can inspect classes, interfaces, fields, and method at runtime with the help of reflection and the best part is that you need not know the names of these classes, methods, etc.

* **什么是依赖注入？** What is Dependency Injection?

* **如何StringBuilder实现 a 来避免不可变字符串分配问题？** - [英文资料](https://stackoverflow.com/questions/54023816/how-is-a-stringbuilder-implemented-to-avoid-the-immutable-string-allocation-prob)  How is a `StringBuilder` implemented to avoid the immutable string allocation problem?

* **StringBuffer和之间的区别StringBuilder？** Difference between `StringBuffer` and `StringBuilder`?

* **Java 中的快速失败迭代器和故障安全迭代器有什么区别？** What is the difference between fail-fast and fail-safe iterators in Java?
    - 故障安全迭代器不会抛出任何异常，即使在迭代集合时修改了集合。但是在故障安全迭代器中，当您在使用集合时尝试修改集合时，它会抛出 ConcurrentModificationException。  Fail-safe iterator will not throw any exception even if the collection is modified while iteration over it. But in Fail-safe iterator, it throws a ConcurrentModificationException when you try to modify the collection while using it.

* **监控与同步**  Monitor and Synchronization

* **说说 Kotlin 的一些优点**  Tell some advantages of Kotlin.

* **val和 和有什么不一样var？** - [英文资料](https://stackoverflow.com/questions/44200075/val-and-var-in-kotlin)   What is the difference between `val` and `var`?

* **在 Kotlin 中使用有什么优势const？** - [视频](https://www.youtube.com/watch?v=3G49ivVxfkU) and [博客](https://amitshekhar.me/blog/const-in-kotlin) What is the advantage of using `const` in Kotlin?

* **什么是 Kotlin 中的 JvmStatic 注解？**[视频](https://www.youtube.com/watch?v=qBBbOhY_pv4) and [博客](https://amitshekhar.me/blog/jvmstatic-annotation-in-kotlin) What is a JvmStatic Annotation in Kotlin?

* **什么是 Kotlin 中的 JvmField 注解？** - [视频](https://www.youtube.com/watch?v=bx8OZcMbeUE) and [博客](https://amitshekhar.me/blog/jvmfield-annotation-in-kotlin) What is a JvmField Annotation in Kotlin?

* **什么是 Kotlin 中的 JvmOverloads 注解？** - [视频](https://www.youtube.com/watch?v=fHGsBV9Za8M) and [博客](https://amitshekhar.me/blog/jvmoverloads-annotation-in-kotlin) What is a JvmOverloads Annotation in Kotlin?

* **如何确保nullKotlin 的安全性？**  How to ensure `null` safety in Kotlin?

* **什么时候使用lateintKotlin 中使用的关键字？**[英文资料](https://amitshekhar.me/blog/lateinit-vs-lazy-in-kotlin)   When to use `lateint` keyword used in Kotlin?

* **如何检查一个lateinit变量是否已经初始化？**[英文资料](https://amitshekhar.me/blog/lateinit-vs-lazy-in-kotlin)   How to check if a `lateinit` variable has been initialized?

* **如何在 Kotlin 中对变量进行延迟初始化？** - [英文资料](https://amitshekhar.me/blog/lateinit-vs-lazy-in-kotlin)  How to do lazy initialization of variables in Kotlin?

* **companion objects科特林有什么？** - [英文资料](https://amitshekhar.me/blog/companion-object-in-kotlin)  What are `companion objects` in Kotlin?

* **Kotlin 中 == 和 ===** [Video](https://www.youtube.com/watch?v=lJtgxT2OIgQ) and [Blog](https://amitshekhar.me/blog/structural-and-referential-equality-in-kotlin) Difference between == and === in Kotlin

* **Kotlin 中的可见性修饰符什么是？** What are the visibility modifiers in Kotlin?

* **Kotlin 中 Java 静态方法的等价物什么是？** What is the equivalent of Java static methods in Kotlin?

* **Kotlin 中的数据类什么是？**  What is a data class in Kotlin?

* **如何在 Kotlin 中创建单例类？** How to create a Singleton class in Kotlin?

* **open和publicKotlin之间有什么区别？** - [英文资料](https://amitshekhar.me/blog/open-keyword-in-kotlin)  What is the difference between `open` and `public` in Kotlin?

* **let解释, run, with, also,apply在 Kotlin 中的用例。** Explain the use-case of `let`, `run`, `with`, `also`, `apply` in Kotlin.

* **Kotlin 中列表和数组类型的区别** Difference between List and Array types in Kotlin

* **Labels科特林有什么？**What are `Labels` in Kotlin?

* **initKotlin 中的块什么是？** - [Video](https://www.youtube.com/watch?v=cb3jOFozJns) and [Blog](https://amitshekhar.me/blog/init-block-in-kotlin) What is an `init` block in Kotlin?

* **在 Kotlin 中解释pair和triple**  Explain `pair` and `triple` in Kotlin.

* **apply和之间如何选择with？** How to choose between `apply` and `with`?

* **switch与之间如何选择when？** How to choose between `switch` with `when`?

* **Kotlin 中的协程什么是？** - [英文资料](https://amitshekhar.me/blog/kotlin-coroutines)  What are Coroutines in Kotlin?

* **什么是协程作用域？** - [英文资料](https://amitshekhar.me/blog/kotlin-coroutines)  What is Coroutine Scope?

* **什么是协程上下文？** - [英文资料](https://amitshekhar.me/blog/kotlin-coroutines)  What is Coroutine Context?

* **在 Kotlin 协程中启动与异步** [英文资料](https://amitshekhar.me/blog/launch-vs-async-in-kotlin-coroutines)  Launch vs Async in Kotlin Coroutines

* **Kotlin 中的内联函数什么是？** - [Video](https://www.youtube.com/watch?v=GLLI8h67ryo) and [Blog](https://amitshekhar.me/blog/inline-function-in-kotlin)What is inline function in Kotlin?

* **什么时候使用 Kotlin 密封类？** When to use Kotlin sealed classes?

* **在 Kotlin 中用接收器解释函数文字？** Explain function literals with receiver in Kotlin?

* **讲述 Kotlin DSL** Tell about Kotlin DSL.

* **Kotlin 中的高阶函数什么是？**[Kotlin 中的高阶函数和 Lambda](https://amitshekhar.me/blog/higher-order-functions-and-lambdas-in-kotlin)What are higher-order functions in Kotlin?

* **什么是 Kotlin 中的 Lambda** - 英文资料: [Kotlin 中的高阶函数和 Lambda](https://amitshekhar.me/blog/higher-order-functions-and-lambdas-in-kotlin)What are Lambdas in Kotlin

* **讲述 Kotlin 中的集合** Tell about the Collections in Kotlin

<br>

---
<br>

### 九.Kotlin 协程

Kotlin Coroutines for Android Interview 你应该知道的话题：Topics you should know in Kotlin Coroutines for Android Interview:

* coroutines 协程
* suspend 挂起、暂停
* launch, async-await, withContext   启动、异步等待、withContext
* dispatchers 调度员
* scope, context, job 范围、背景、工作
* lifecycleScope, viewModelScope, GlobalScope  
* suspendCoroutine, suspendCancellableCoroutine 
* coroutineScope, supervisorScope  协程作用域、主管作用域

您可以在这里学习这些主题：[Master Kotlin Coroutines](https://amitshekhar.me/blog/kotlin-coroutines)


<br>

---
<br>

### 十.Kotlin Flow API

Android 面试中 Kotlin Flow API 你应该知道的主题： Topics you should know in Kotlin Flow API for Android Interview:

* Flow Builder, Operator, Collector Flow Builder、Operator、Collector
* flowOn, dispatchers flowOn，调度员
* filter、map、zip、flatMapConcat、retry、debounce、distinctUntilChanged、flatMapLatest 等运算符
* Terminal operators
* 冷流与热流 Cold Flow vs Hot Flow: [Cold Flow vs Hot Flow](https://amitshekhar.me/blog/cold-flow-vs-hot-flow)
* [StateFlow, SharedFlow](https://amitshekhar.me/blog/stateflow-and-sharedflow), callbackFlow, channelFlow

您可以在这里学习这些主题：Kotlin Flow API You can learn these topics here: [Kotlin Flow API](https://amitshekhar.me/blog/flow-api-in-kotlin)


<br>

---
<br>

### 十一.Jetpack Compose

您应该在 Jetpack Compose for Android Interview 中了解的主题： Topics you should know in Jetpack Compose for Android Interview:

* Compose 撰写
* 状态：remember, rememberSaveable, MutableState  State: remember, rememberSaveable, MutableState
* Recomposition 重组
* State hoisting 吊装状态
* Side-effects 副作用
* Modifier 修改器
* Theme 主题
* Layout, List 布局、列表
* Gestures, Animation 手势、动画
* CompositionLocal 组合局部

<br>

---
<br>

### 十二.Other Topics 其他主题

安卓面试题：:

* **描述 REST API 的工作原理。什么是REST？**  Describe how REST APIs work. What is REST?

* **描述 SQLite** Describe SQLite.

* **描述数据库** Describe database.

* **您如何控制特定用户数量的应用程序版本更新？** How do you control the application version update to specific number of users?

* **我们可以识别卸载了我们应用程序的用户吗？** Can we identify users who have uninstalled our application?

* **安卓开发最佳实践**[Android 开发最佳实践](https://amitshekhar.me/blog/android-development-best-practices) Android Development Best Practices.

* **你试过Kotlin吗？** Have you tried Kotlin?

* **在 Android 应用程序开发过程中，您应该持续衡量哪些指标？** - 英文资料: [Android 应用程序性能指标](https://amitshekhar.me/blog/android-app-performance-metrics)What are the metrics that you should measure continuously while android application development?

* **什么是 Chrome 自定义标签页？如何在您的应用程序中显示网页内容？** What is Chrome Custom Tabs? How to display web content in your app?

* **如何避免将 API 密钥签入 VCS？**  How to avoid API keys from check-in into VCS?

* **Kotlin Multiplatform 如何工作？** - [英文资料](https://amitshekhar.me/blog/how-does-the-kotlin-multiplatform-work)  How does the Kotlin Multiplatform work?

* **如何使用内存堆转储数据？**  How to use Memory Heap Dumps data?

* **如何在您的应用中实现深色主题？** How to implement Dark Theme in your app?

* **您尝试过 Jetpack 撰写吗？** Have you tried Jetpack compose?

* **如何保护应用程序中使用的 API 密钥？** How to secure the API keys used in an app?

* **如何转换检查 Kotlin 的 Java 等效代码？** How to convert check Java equivalent code of Kotlin?

* **谈谈 Android 中的内存使用情况。** Tell something about memory usage in Android.

* **你能在 Android 中创建透明活动吗？** Can you create transparent activity in Android?

* **解释注解处理。** Explain Annotation processing.

* **如何提高通知传递率？** How to increase the Notification delivery rate?

* **通知系统如何运作？** How does the notification system work?

* **如何在准确时间显示本地通知？** How to show local Notification at an exact time?

<br>

---
<br>

### 十三.Data Structures and Algorithms 数据结构和算法

* **Android 开发人员在下次面试时应该了解这些数据结构**[检查此处](https://amitshekhar.me/blog/android-developer-should-know-these-data-structures-for-next-interview) Android Developer should know these Data Structures for Next Interview

<br>

---
<br>

### 发现这个项目很有用❤️ Found this project useful :heart:

* 支持点击⭐此页面右上角的按钮。✌️ Support by clicking the :star: button on the upper right of this page. :v:

您可以通过以下方式与`amit shekhar`联系： You can connect with me on:

- [Twitter](https://twitter.com/amitiitbhu)
- [YouTube](https://www.youtube.com/@amitshekhar)
- [LinkedIn](https://www.linkedin.com/in/amit-shekhar-iitbhu)
- [GitHub](https://github.com/amitshekhariitbhu)

<br>

---
<br>

### License
```
   Copyright (C) 2022 Amit Shekhar

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
```

<br>

---
<br>

### Contributing to 
Just make pull request. You are in!
