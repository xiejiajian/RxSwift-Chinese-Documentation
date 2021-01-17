# 10.1 文档更新日志

文档变更将被记录在此文件内。

## [2.0.0](https://github.com/beeth0ven/RxSwift-Chinese-Documentation/releases/tag/2.0.0)

### 19年5月21日（RxSwift 5）

* [RxSwift 5 更新了什么？](../recipes/whats_new_in_rxswift_5.md)
* 引入[食谱章节](../recipes/)
* [Signal](../rxswift_core/observable/signal.md)
* [RxRelay](../recipes/rxrelay.md)
* [纯函数](../recipes/pure_function.md)
* [附加作用](../recipes/side_effects.md)
* [共享附加作用](../recipes/share_side_effects.md)
* 更新文档以适配 RxSwift 5
* 更新 QQ 群号为：871293356

## [1.2.0](https://github.com/beeth0ven/RxSwift-Chinese-Documentation/releases/tag/1.2.0)

### 18年2月15日

* 纠正错别字
* 给 [retry](../decision_tree/retry.md) 操作符加入演示代码
* 给 [replay](../decision_tree/replay.md) 操作符加入演示代码
* 给 [connect](../decision_tree/connect.md) 操作符加入演示代码
* 给 [publish](../decision_tree/publish.md) 操作符加入演示代码
* 给 [reduce](../decision_tree/reduce.md) 操作符加入演示代码
* 给 [skipUntil](../decision_tree/skipuntil.md) 操作符加入演示代码
* 给 [skipWhile](../decision_tree/skipwhile.md) 操作符加入演示代码
* 给 [skip](../decision_tree/skip.md) 操作符加入演示代码

## [1.1.0](https://github.com/beeth0ven/RxSwift-Chinese-Documentation/releases/tag/1.1.0)

### 17年12月7日

* 纠正错别字
* 给 [takeUntil](../decision_tree/takeuntil.md) 操作符加入演示代码
* 给 [takeWhile](../decision_tree/takewhile.md) 操作符加入演示代码
* 给 [takeLast](../decision_tree/takelast.md) 操作符加入演示代码
* 加入 [debug](../decision_tree/debug.md) 操作符
* 给 [AsyncSubject](../rxswift_core/observable_and_observer/async_subject.md) 加入演示代码
* 给 [take](../decision_tree/take.md) 操作符加入演示代码
* 给 [elementAt](../decision_tree/elementat.md) 操作符加入演示代码
* 给 [BehaviorSubject](../rxswift_core/observable_and_observer/behavior_subject.md) 加入演示代码

## [1.0.0](https://github.com/beeth0ven/RxSwift-Chinese-Documentation/releases/tag/1.0.0)

### 17年10月18日（RxSwift 4）

* 加入[文档电子书下载地址](https://github.com/beeth0ven/RxSwift-Chinese-Documentation/releases/download/1.0.0/RxSwiftChineseDocumentation.epub)
* 去掉学习资源[《如何将代理转换为序列》](https://medium.com/@maxofeden/rxswift-migrate-delegates-to-beautiful-observables-3e606a863048)，因为 RxSwift 4 重构了 **DelegateProxy**  [\#1379](https://github.com/ReactiveX/RxSwift/pull/1379)
* 使用 `share(replay: 1)` 替换 `shareReplay(1)`
* 给 [RxJava 演示代码](../rxswift_ecosystem.md) 中的变量加上 `final` 关键字，声明为常量
* 示例[多层级的列表页](../more_demo/tableview_sectioned_viewcontroller.md)更新到 RxSwift 4，使用新的 RxDataSources 构建方法
* 文档[首页](../introduction.md)更新到 RxSwift 4

## [0.2.0](https://github.com/beeth0ven/RxSwift-Chinese-Documentation/releases/tag/0.2.0)

### 17年10月9日

* 给 [ReplaySubject](../rxswift_core/observable_and_observer/replay_subject.md) 加入演示代码
* 给 [PublishSubject](../rxswift_core/observable_and_observer/publish_subject.md) 加入演示代码
* 给 [distinctUntilChanged](../decision_tree/distinctuntilchanged.md) 操作符加入演示代码
* 给 [scan](../decision_tree/scan.md) 操作符加入演示代码
* 给 [startWith](../decision_tree/startwith.md) 操作符加入演示代码
* 给 [merge](../decision_tree/merge.md) 操作符加入演示代码
* **\(RxSwift 4\)** 使用 [Binder](../rxswift_core/observer/binder.md) 替换 **UIBindingObserver**，更简洁实用

## [0.1.1](https://github.com/beeth0ven/RxSwift-Chinese-Documentation/releases/tag/0.1.1)

### 17年9月18日

* 更新 [RxFeedback](../architecture/rxfeedback/) 配图，与官方保持一致
* 修复 [Maybe](../rxswift_core/observable/maybe.md) 中的[描述问题](https://github.com/beeth0ven/RxSwift-Chinese-Documentation/pull/9/files)

## [0.1.0](https://github.com/beeth0ven/RxSwift-Chinese-Documentation/releases/tag/0.1.0)

### 17年9月4日

* 加入学习资源[《泊学 RxSwift 中文视频教程》](https://boxueio.com/series/rxswift-101)
* 给 [concat](../decision_tree/concat.md) 操作符加入演示代码
* 给 [concatMap](../decision_tree/concatmap.md) 操作符加入演示代码
* 将操作符列表移动到[《如何选择操作符？》](../decision_tree/)章节下，便于查找
* 给 [combineLatest](../decision_tree/combinelatest.md) 操作符加入演示代码
* 给 [catchError](../decision_tree/catcherror.md) 操作符加入演示代码
* 给 [filter](../decision_tree/filter.md) 操作符加入演示代码
* 给 [flatMap](../decision_tree/flatmap.md) 操作符加入演示代码
* 给 [flatMapLatest](../decision_tree/flatmaplatest.md) 操作符加入演示代码
* 给 [map](../decision_tree/map.md) 操作符加入演示代码
* 给 [zip](../decision_tree/zip.md) 操作符加入演示代码
* 给 [withLatestFrom](../decision_tree/withlatestfrom.md) 操作符加入演示代码

## [0.0.1](https://github.com/beeth0ven/RxSwift-Chinese-Documentation/releases/tag/0.0.1)

### 17年9月1日（RxSwift 3.6.1）

* 加入 56 个[操作符](../rxswift_core/operator.md)中文说明
* 加入[图片选择器](../more_demo/image_picker.md)示例
* 加入[多层级的列表页](../more_demo/tableview_sectioned_viewcontroller.md)示例
* 加入[计算器](../more_demo/calculator.md)示例
* 加入 [MVVM](../architecture/mvvm/) 架构
* 加入 [RxFeedback](../architecture/rxfeedback/) 架构
* 加入 [ReactorKit](../architecture/reactorkit/) 架构
* 加入 [RxSwift 生态系统和 ReactiveX 生态系统](../rxswift_ecosystem.md) 章节
* 加入文档更新日志
* 加入学习资源[《几个 share 操作符的区别》](https://medium.com/@_achou/rxswift-share-vs-replay-vs-sharereplay-bea99ac42168)
* 加入学习资源[《如何将代理转换为序列》](https://medium.com/@maxofeden/rxswift-migrate-delegates-to-beautiful-observables-3e606a863048)

