在我们开始之前，我想提一下，我发布了一个视频播放列表来帮助你破解 Android 面试：[查看Android 面试问题和答案](https://www-youtube-com.translate.goog/playlist?list=PL_I3TGB7aK6jNBMZkw3FYdJXyf7quHdI8&_x_tr_sl=auto&_x_tr_tl=zh-CN&_x_tr_hl=zh-CN&_x_tr_pto=wapp)

本文适用于对Kotlin 协程感到好奇但不知道它到底是什么的任何人。目的是让您了解什么是 Kotlin Coroutines，这意味着在编写本文时几乎没有做任何简化。如果您了解什么是 Kotlin 协程，那么我的任务就完成了。如果您完整地阅读了这篇文章，我相信我的任务将会完成。

>知识来到那些渴望它的人。

在本教程中，我们将通过涵盖以下主题来掌握 Android 中的 **Kotlin协程**：

* 什么是协程？
* 为什么需要 Kotlin Coroutines 提供的解决方案?
* 有关如何在 Android 中实现 Kotlin 协程的分步指南。 
* 在 Kotlin 协程中启动与异步 Kotlin 协程中的作用域是什么？
* Kotlin 协程中的异常处理。
* 通过 [示例](https://github.com/amitshekhariitbhu/Learn-Kotlin-Coroutines) 学习适用于 Android 的 Kotlin 协程的项目。

当前可用于处理多线程的框架导致回调地狱和阻塞状态，因为我们没有任何其他简单的方法来保证线程安全执行。

协程是一个非常高效和完整的框架，可以以更高效和更简单的方式管理并发。

让我们以一种非常简单的方式了解协程到底是什么。

### 什么是协程？

**Coroutines** = Co + Routines

在这里，Co 表示合作，Routines 表示功能。

这意味着当函数相互协作时，我们称之为**协程**。


协作协程
让我们用一个例子来理解这一点。为了便于理解，我以不同的方式编写了以下代码。假设我们有两个函数 **functionA** 和 **functionB** 。

**functionA** 如下：
```kotlin
fun functionA(case: Int) {
    when (case) {
        1 -> {
            taskA1()
            functionB(1)
        }
        2 -> {
            taskA2()
            functionB(2)
        }
        3 -> {
            taskA3()
            functionB(3)
        }
        4 -> {
            taskA4()
            functionB(4)
        }
    }
}
```

如下 **functionB** 所示：
```kotlin
fun functionB(case: Int) {
    when (case) {
        1 -> {
            taskB1()
            functionA(2)
        }
        2 -> {
            taskB2()
            functionA(3)
        }
        3 -> {
            taskB3()
            functionA(4)
        }
        4 -> {
            taskB4()
        }
    }
}
```
然后，我们可以调用 **functionA** 如下：
```kotlin
functionA(1)
```
在这里，**functionA** 将做 **taskA1** 交给控制 **functionB** 执行 **taskB1** 。

然后， **functionB** 将执行 **taskB1** 并将控制权交还给 **functionA** 执行 **taskA2** 等等。

重要的是， **functionA** 他们 **functionB** 彼此合作。

使用 Kotlin 协程，可以非常轻松地完成上述协作，而无需使用我在上面的示例中为了理解而使用的 **when** 或 **switch case**  。

现在，我们已经了解了函数之间协作时什么是协程。由于功能的协作性质，存在无限的可能性。

一些可能性如下：

它可以执行几行  **functionA** ，然后执行几行 **functionB** ，然后再执行几行  **functionA** ，依此类推。当一个线程处于空闲状态并且什么都不做时，这将很有帮助，在这种情况下，它可以执行另一个函数的几行。这样，它就可以充分利用线程。最终合作有助于多任务处理。

它将支持以同步方式编写异步代码。我们将在本文后面讨论这个。
总的来说，协程使多任务处理变得非常容易。

所以，我们可以说**协程和线程都是多任务**的。但不同的是，**线程由操作系统管理，协程由用户管理**，因为它可以利用协作执行几行功能。

**_协程是一个基于实际线程编写的优化框架_**，利用函数的协作特性使其轻巧而强大。所以，我们可以说**协程是轻量级的线程**。轻量级线程意味着它不映射到本机线程，因此不需要在处理器上进行上下文切换，因此它们速度更快。

### 协程不映射到本机线程

当我说“**协程不映射到本机线程**”时，它是什么意思？

协程有多种语言版本。基本上，有两种类型的协程：

1. Stackless 无堆叠
2. Stackful 堆积如山

Kotlin 实现无堆栈协程——这意味着协程没有自己的堆栈，因此它们不会映射到本机线程。

现在，你可以理解下面这段话，Kotlin 官方网站上说的是什么

**可以将协程视为一种轻量级线程。和线程一样，协程可以并行运行，相互等待和通信。最大的区别是协程非常便宜，几乎是免费的：我们可以创建成千上万个协程，并且在性能方面支付的费用很少。另一方面，真正的线程的启动和维护成本很高。一千个线程对于现代机器来说可能是一个严峻的挑战。**

**协程并没有取代线程，它更像是一个框架来管理它们.**

**Coroutines 的确切定义：一种以更高效和更简单的方式管理并发的框架，其轻量级线程编写在实际线程框架之上，通过利用函数的协作性质来充分利用它。**

现在，我们已经了解了协程到底是什么。现在我们需要知道为什么需要 Kotlin Coroutines 提供的解决方案。

### 为什么需要 Kotlin 协程？

让我们来看一个非常标准的 Android 应用程序用例，如下所示：

* 从服务器获取用户。
* 在 UI 中显示用户。
```kotlin
fun fetchAndShowUser() {
    val user = fetchUser()
    showUser(user)
}

fun fetchUser(): User {
    // make network call
    // return user
}

fun showUser(user: User) {
    // show user
}
```
当我们调用该```fetchAndShowUser```函数时，它会抛出异常```NetworkOnMainThreadException```，因为主线程不允许进行网络调用。

有很多方法可以解决这个问题。其中一些如下：

**1.使用回调**：在这里，我们在后台线程中运行 fetchUser 并通过回调传递结果。
```kotlin
fun fetchAndShowUser() {
    fetchUser { user ->
        showUser(user)
    }
}

fun fetchUser(callback: (User) -> Unit)) {
    // make network call on background thread to get user
    // callback with user
    callback(user)
}

fun showUser(user: User) {
    // show user
}
```
让我们看另一个例子，其中我们有三个嵌套的网络调用。

```kotlin
fun fetchData() {
    fetchA { a ->
        fetchB(a) { b ->
            fetchC(b) { c ->
                // do something with c
            }
        }
    }
}
```
这种类型的嵌套也称为 - “回调地狱”。

**2.使用 RxJava**：反应世界的方法。这样我们就可以摆脱嵌套的回调。
```kotlin
fetchUser()
    .subscribeOn(Schedulers.io())
    .observerOn(AndroidSchedulers.mainThread())
    .subscribe { user ->
        showUser(user)
    }

fun fetchUser(): Single<User> {
    // make network call
    // emit user
}

fun showUser(user: User) {
    // show user
}
```

**3.使用协程**：是的，协程。
```kotlin
fun fetchAndShowUser() {
    GlobalScope.launch(Dispatchers.Main) {
        val user = fetchUser() // fetch on IO thread
        showUser(user) // back on UI thread
    }
}

suspend fun fetchUser(): User {
    return withContext(Dispatchers.IO) {
        // make network call on IO thread
        // return user
    }
}

fun showUser(user: User) {
    // show user
}
```
这里，上面的代码看起来是同步的，其实是异步的。我们将看看这怎么可能。

通过编写 **launch**，我们启动协程来执行任务。
```kotlin
GlobalScope.launch {
    // do something here
}
```

### Kotlin协程在Android中的实现

在 Android 项目中添加 Kotlin Coroutines 依赖，如下所示：
```kotlin
dependencies {
    implementation "org.jetbrains.kotlinx:kotlinx-coroutines-core:x.x.x"
    implementation "org.jetbrainskotlinx:kotlinx-coroutines-android:x.x.x"
}
```

让我们看看上面例子中出现的所有函数：

功能 **fetchAndShowUser**：
```kotlin
fun fetchAndShowUser() {
    GlobalScope.launch(Dispatchers.Main) {
        val user = fetchUser() // fetch on IO thread
        showUser(user) // back on UI thread
    }
}
```

功能 **fetchUser**：
```kotlin
suspend fun fetchUser(): User {
    return withContext(Dispatchers.IO) {
        // make network call on IO thread
        // return user
    }
}
```
和 **showUser** 功能：
```kotlin
fun showUser(user: User) {
    // show user
}
```
注意：我已经使用 GlobalScope 作为快速示例，我们应该不惜一切代价避免使用它。在 Android 项目中，我们应该根据我们的用例使用自定义范围，例如 **lifecycleScope** , **viewModelScope** 等。我们将在下面的范围部分了解它们。

别着急，我们将在本文中逐步学习 **suspend**、**GlobalScope**、**withContext** 和 **Dispatchers.IO**。

我们在这里介绍了两个东西如下：

**1.Dispatchers**：Dispatchers 帮助协程决定工作必须在哪个线程上完成。主要有三种类型的 Dispatcher，分别是**IO**、**Default** 和 **Main**。 IO dispatcher 用于做网络和磁盘相关的工作。默认值用于执行 CPU 密集型工作。
Main是Android的UI线程。
如果您想了解有关 Dispatchers 的更多信息：[Kotlin 协程中的调度程序 Dispatchers]()。

**2.suspend**：暂停功能是可以启动、暂停和恢复的功能。

### 挂起函数协程

**挂起函数只允许从协程或另一个挂起函数中调用**。您可以看到该函数 **fetchUser** 包含关键字suspend。因此，为了使用它，我们从协程中调用了它。

现在，如果需要，我们如何在 **Activity** 里的 **onCreate** 调用 **fetchUser** ？

因为 **fetchUser** 只能从另一个挂起函数或协程调用。我们不能让  **Activity** 的**onCreate** 方法挂起，所以我们需要从协程中调用它（通过启动协程），如下所示：
```kotlin
override fun onCreate(savedInstanceState: Bundle?) {
super.onCreate(savedInstanceState)

    GlobalScope.launch(Dispatchers.Main) {
        val user = fetchUser() // fetch on IO thread
        showUser(user) // back on UI thread
    }

}
```
**fetchUser**将在 IO 线程上运行，因为我们已经将Dispatchers.IO与withContext.

**showUser**将在 UI 线程上运行，因为我们已经使用Dispatchers.Main启动调用它的协程。

让我们再举一个简单的例子来进一步了解它。
```kotlin
class MainActivity : AppCompatActivity() {

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)

        GlobalScope.launch(Dispatchers.Main) {
            doSomething() // non-suspend, UI thread
            doLongRunningTask() // suspend, Default background thread
            doSomethingElse() // non-suspend, UI thread
        }

    }

    fun doSomething() {

    }

    fun doSomethingElse() {

    }

    suspend fun doLongRunningTask() {
        withContext(Dispatchers.Default) {
            // code for doing a long running task
            // Added delay to simulate
            delay(2000)
        }
    }

}
```
在这里，我们有 3 个函数，其中只有一个函数是挂起函数。

**doSomething**：非暂停功能
**doLongRunningTask**：挂起函数
**doSomethingElse**：非暂停功能
在这种情况下，非挂起函数**doSomething**将**doSomethingElse**在 UI 线程上运行，因为我们已经使用Dispatchers.Main启动调用它们的协程。

并且挂起函数doLongRunningTask将在默认后台线程上运行，因为我们已经将Dispatchers.Default与withContext.

在这里，我们使用Dispatchers.Main启动协程，首先它从 UI 线程开始，它将在 UI 线程上执行函数，doSomething因为这是一个非挂起函数。目前，我们可以说控制权在UI Thread手中。

那么，就会遇到doLongRunningTasksuspend函数。它使用 Default 后台线程启动协程，因为我们已经将Dispatchers.Default与withContext. 目前，我们可以说控制权在Default Thread手中。

之后，当长任务完成时，控制权将交还给 UI 线程，因为我们又有了一个非挂起函数doSomethingElse。此函数将在 UI 线程上执行。

简而言之，我们在 UI 上下文中启动一个新协程launch(Dispatchers.Main)，首先在 UI 线程上做一些事情，然后调用挂起函数在doLongRunningTask不阻塞主 UI 线程的情况下执行异步长任务，然后再次在 UI 线程上做一些其他事情。

这就是看起来同步的代码是异步的。只有 Kotlin 中的协程才有可能。这就是 Kotlin 协程的美妙之处。

现在，让我们了解启动协程的不同方法。

Kotlin 中有两个启动协程的函数，分别是：
```kotlin
launch{}
async{}
```
在 Kotlin 协程中启动与异步
不同之处在于，launch{}返回 aJob并且不携带任何结果值，而async{}返回一个实例Deferred<T>，它有一个await()返回协程结果的函数，就像我们在 Java 中有未来一样，我们可以在其中future.get()获取结果。

换句话说：

发射：发射后忘记
异步：执行任务并返回结果
让我们举个例子来学习启动和异步。

我们可以使用启动如下：
```kotlin
GlobalScope.launch(Dispatchers.Default) {
// do something and do not return result
}
```
但是当我们需要返回结果时，我们需要使用async。
```kotlin
val deferred = GlobalScope.async(Dispatchers.Default) {
// do something and return result, for example 10 as a result
return@async 10
}
val result = deferred.await() // result = 10
```
在这里，我们使用await().

所以，现在，我们已经了解了启动函数和异步函数之间的区别。详细了解差异：Launch vs Async in Kotlin Coroutines

有一种叫做withContext 的东西。

withContext是一个挂起函数，通过它我们可以通过提供Dispatchers我们希望任务完成的时间来完成任务。

withContext不创建新的协程，它只改变现有协程的上下文，它是一个挂起函数，而launch创建async一个新的协程，它们不是挂起函数。

让我们看看 的代码withContext。
```kotlin
private suspend fun doLongRunningTaskAndDoNotReturnResult() {
withContext(Dispatchers.Default) {
// your code for doing a long running task
// Added delay to simulate
delay(2000)
}
}
```
它还可以返回结果。
```kotlin
private suspend fun doLongRunningTask(): Int {
return withContext(Dispatchers.Default) {
// your code for doing a long running task
// Added delay to simulate
delay(2000)
return@withContext 10
}
}
```
与挂起函数一样withContext，它只能从挂起函数或协程中调用。所以，以上两个函数都是挂起函数。

让我们看一个使用上述函数的例子：
```kotlin
GlobalScope.launch(Dispatchers.Main) {
val result = doLongRunningTask()
showResult(result) // back on UI thread
}
```
现在，让我们有两个长时间运行的任务和结果。
```kotlin
private suspend fun doLongRunningTaskOne(): Int {
return withContext(Dispatchers.Default) {
// your code for doing a long running task
// Added delay to simulate
delay(2000)
return@withContext 10
}
}
private suspend fun doLongRunningTaskTwo(): Int {
return withContext(Dispatchers.Default) {
// your code for doing a long running task
// Added delay to simulate
delay(2000)
return@withContext 10
}
}
```
让我们看一个使用上述两个函数的例子。
```kotlin
GlobalScope.launch(Dispatchers.Main) {
val resultOne = doLongRunningTaskOne()
val resultTwo = doLongRunningTaskTwo()
showResult(resultOne + resultTwo) // back on UI thread
}
```
在这里，大约 4000 毫秒后，它将显示结果，因为它将完成第一个任务，然后才开始第二个任务。

现在，假设我们必须并行执行这两项任务，因此我们将不得不启动两个协程。因此，我们可以使用launch或async来启动协程。在这里，因为我们需要从任务中返回结果，所以我们必须执行async以下操作：
```kotlin
GlobalScope.launch {

    val deferredOne = async {
        doLongRunningTaskOne()
    }

    val deferredTwo = async {
        doLongRunningTaskTwo()
    }

    val result = deferredOne.await() + deferredTwo.await()

    showResult(result) // back on UI thread

}
```
在这里，我们使用 启动两个协程async，因此两个任务将并行运行。仅在大约 2000 毫秒后，它将显示结果，因为它将并行运行两个任务。

经验法则：

和 都launch用于async启动协程。这使我们能够并行执行任务。
async可用于获得 . 无法获得的结果launch。
withContext不启动协程，它只是一个suspend用于转换现有协程上下文的函数。
我们稍后将在本博客中了解异常处理。

Kotlin 协程中的作用域
Kotlin Coroutines 中的作用域非常有用，因为我们需要在 Activity 被销毁后立即取消后台任务。在这里，我们将学习如何使用范围来处理这些类型的情况。

在特定于 Android 的项目中，我们应该使用通过考虑 Activity、ViewModel 等的生命周期而创建的自定义范围。

作用域位于 kotlin 扩展库下。确保将所需的依赖项添加到您的项目中。

活动范围示例

假设我们的活动是范围，一旦活动被销毁，后台任务就应该被取消。

在活动中，我们应该使用lifecycleScope来启动协程。
```kotlin
class MainActivity : AppCompatActivity() {

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)

        lifecycleScope.launch {
            val user = fetchUser()
            // show user
        }

    }

    suspend fun fetchUser(): User {
        return withContext(Dispatchers.IO) {
            // fetch user
            // return user
        }
    }

}
```
一旦 Activity 被销毁，如果它正在运行，任务将被取消，因为我们已经使用了绑定到 Activity 的 LifeCycle 的范围。

ViewModel 范围示例

假设我们的 ViewModel 是作用域，一旦 ViewModel 被销毁，后台任务就应该被取消。

在 ViewModel 中，我们应该使用viewModelScope协程来启动。
```kotlin
class MainViewModel : ViewModel() {

    fun fetch() {
        viewModelScope.launch {
            val user = fetchUser()
            // show user
        }
    }

    suspend fun fetchUser(): User {
        return withContext(Dispatchers.IO) {
            // fetch user
            // return user
        }
    }

}
```
一旦 ViewModel 被销毁，如果任务正在运行，它就会被取消，因为我们已经使用了绑定到 ViewModel 的生命周期的范围。

这就是 Kotlin 协程中的范围非常有用的原因。

Kotlin 协程中的异常处理
异常处理是另一个重要的话题。我们必须学习这一点。

使用启动时

```kotlin
suspend fetchUserAndSaveInDatabase() {
withContext(Dispatchers.IO) {
// fetch user
// save in database
}
}
```
一种方法是使用 try-catch 块：
```kotlin
GlobalScope.launch(Dispatchers.Main) {
try {
fetchUserAndSaveInDatabase() // do on IO thread and back to UI Thread
} catch (exception: Exception) {
Log.d(TAG, "$exception handled !")
}
}
```
另一种方法是使用处理程序：

为此，我们需要创建一个异常处理程序，如下所示：
```kotlin
val handler = CoroutineExceptionHandler { _, exception ->
Log.d(TAG, "$exception handled !")
}
```
然后，我们可以附加处理程序如下：
```kotlin
GlobalScope.launch(Dispatchers.Main + handler) {
fetchUserAndSaveInDatabase() // do on IO thread and back to UI Thread
}
```
如果 中有异常fetchUserAndSaveInDatabase，它将由我们附加的处理程序处理。

使用异步时

使用异步时，我们需要使用 try-catch 块来处理异常，如下所示。
```kotlin
val deferredUser = GlobalScope.async {
fetchUser()
}
try {
val user = deferredUser.await()
} catch (exception: Exception) {
Log.d(TAG, "$exception handled !")
}
```
现在，让我们看看 Android 开发中异常处理的一些更真实的用例。

假设，我们有两个网络调用如下：

getUsers()
getMoreUsers()
两者都是暂停功能。

而且，我们正在按如下顺序进行网络调用：
```kotlin
launch {
try {
val users = getUsers()
val moreUsers = getMoreUsers()
} catch (exception: Exception) {
Log.d(TAG, "$exception handled !")
}
}
```
如果其中一个网络调用失败，它将直接进入区块catch。

但是假设，我们想为失败的网络调用返回一个空列表，并继续其他网络调用的响应。我们可以将try-catch块添加到单独的网络调用中，如下所示：
```kotlin
launch {
val users = try {
getUsers()
} catch (e: Exception) {
emptyList<User>()
}
val moreUsers = try {
getMoreUsers()
} catch (e: Exception) {
emptyList<User>()
}
}
```
这样，如果出现任何错误，它将继续使用空列表。

现在，如果我们想并行进行网络调用怎么办？我们可以使用async.
```kotlin
launch {
try {
val usersDeferred = async {  getUsers() }
val moreUsersDeferred = async { getMoreUsers() }
val users = usersDeferred.await()
val moreUsers = moreUsersDeferred.await()
} catch (exception: Exception) {
Log.d(TAG, "$exception handled !")
}
}
```
在这里，我们将面临一个问题，如果出现任何网络错误，应用程序将崩溃！，它不会去块catch。

为了解决这个问题，我们将不得不使用coroutineScope如下：
```kotlin
launch {
try {
coroutineScope {
val usersDeferred = async {  getUsers() }
val moreUsersDeferred = async { getMoreUsers() }
val users = usersDeferred.await()
val moreUsers = moreUsersDeferred.await()
}
} catch (exception: Exception) {
Log.d(TAG, "$exception handled !")
}
}
```
现在，如果出现任何网络错误，它将进入区块catch。

但是再次假设，我们想要为失败的网络调用返回一个空列表，并继续使用来自其他网络调用的响应。我们将不得不使用supervisorScope并将块添加try-catch到单独的网络调用中，如下所示：
```kotlin
launch {
supervisorScope {
val usersDeferred = async { getUsers() }
val moreUsersDeferred = async { getMoreUsers() }
val users = try {
usersDeferred.await()
} catch (e: Exception) {
emptyList<User>()
}
val moreUsers = try {
moreUsersDeferred.await()
} catch (e: Exception) {
emptyList<User>()
}
}
}
```
同样，这样，如果出现任何错误，它将继续使用空列表。

这就是supervisorScope帮助。

结论：

在不使用 的同时async，我们可以继续使用 thetry-catch或 theCoroutineExceptionHandler并根据我们的用例实现任何目标。
在使用 时async，除了try-catch，我们还有两个选择：coroutineScope和supervisorScope。
With async，supervisorScope用于每个任务的个人try-catch，当您希望在其中一个或某些任务失败时继续执行其他任务时。
With ，与顶级一起async使用，当您不想继续执行其他任务（如果其中任何一个失败）时。coroutineScopetry-catch
主要区别在于协程范围将在其任何子级失败时取消。如果我们想在一个任务失败时继续执行其他任务，我们可以使用 supervisorScope。当其中一个失败时，supervisorScope 不会取消其他孩子。

如果您想了解有关 coroutineScope 和 supervisorScope 的更多信息：检查coroutineScope 与 supervisorScope。

这就是在 Kotlin 协程中进行异常处理的方式。

我认为我们今天已经获得了很多知识。非常感谢您的参与。

现在，让我们开始使用 Kotlin 协程。

通过示例学习适用于 Android 的 Kotlin 协程的项目：学习 Kotlin 协程

请与您的开发人员同行分享此博客以传播知识。

从这里学习 Kotlin Flow：Kotlin Flow

就这样吧。
