# 4.6 Schedulers - 调度器

![](../.gitbook/assets/Scheduler.png)

**Schedulers** 是 **Rx** 实现多线程的核心模块，它主要用于控制任务在哪个线程或队列运行。

如果你曾经使用过 [GCD](https://developer.apple.com/library/content/documentation/General/Conceptual/ConcurrencyProgrammingGuide/OperationQueues/OperationQueues.html#//apple_ref/doc/uid/TP40008091-CH102-SW1)， 那你对以下代码应该不会陌生：

```swift
// 后台取得数据，主线程处理结果
DispatchQueue.global(qos: .userInitiated).async {
    let data = try? Data(contentsOf: url)
    DispatchQueue.main.async {
        self.data = data
    }
}
```

如果用 **RxSwift** 来实现，大致是这样的：

```swift
let rxData: Observable<Data> = ...

rxData
    .subscribeOn(ConcurrentDispatchQueueScheduler(qos: .userInitiated))
    .observeOn(MainScheduler.instance)
    .subscribe(onNext: { [weak self] data in
        self?.data = data
    })
    .disposed(by: disposeBag)
```

## 使用 [subscribeOn](../decision_tree/subscribeon.md)

我们用 [subscribeOn](../decision_tree/subscribeon.md) 来决定数据序列的构建函数在哪个 **Scheduler** 上运行。以上例子中，由于获取 `Data` 需要花很长的时间，所以用 [subscribeOn](../decision_tree/subscribeon.md) 切换到 **后台 Scheduler** 来获取 `Data`。这样可以避免主线程被阻塞。

## 使用 [observeOn](../decision_tree/observeon.md)

我们用 [observeOn](../decision_tree/observeon.md) 来决定在哪个 **Scheduler** 监听这个数据序列。以上例子中，通过使用 [observeOn](../decision_tree/observeon.md) 方法切换到主线程来监听并且处理结果。

一个比较典型的例子就是，在后台发起网络请求，然后解析数据，最后在主线程刷新页面。你就可以先用 [subscribeOn](../decision_tree/subscribeon.md) 切到后台去发送请求并解析数据，最后用 [observeOn](../decision_tree/observeon.md) 切换到主线程更新页面。

## MainScheduler

MainScheduler 代表**主线程**。如果你需要执行一些和 UI 相关的任务，就需要切换到该 Scheduler 运行。

## SerialDispatchQueueScheduler

SerialDispatchQueueScheduler 抽象了**串行** `DispatchQueue`。如果你需要执行一些串行任务，可以切换到这个 Scheduler 运行。

## ConcurrentDispatchQueueScheduler

ConcurrentDispatchQueueScheduler 抽象了**并行** `DispatchQueue`。如果你需要执行一些并发任务，可以切换到这个 Scheduler 运行。

## OperationQueueScheduler

OperationQueueScheduler 抽象了 `NSOperationQueue`。

它具备 `NSOperationQueue` 的一些特点，例如，你可以通过设置 `maxConcurrentOperationCount`，来控制同时执行并发任务的最大数量。

