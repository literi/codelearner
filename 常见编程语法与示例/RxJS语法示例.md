### RxJs简介
    RxJS 是 ReactiveX 编程理念的 JavaScript 版本。ReactiveX 来自微软，它是一种针对异步数据流的编程，它的本质是工具库，处理的是事件流，相当于lodash。

### 核心概念

-   Observables 
   
    被观察者，用来产生消息/数据,Observable 是一等公民，将一切问题都转化为 Observable 去处理

-   Observer/Subscriber   
    
    观察者,用来消费消息/数据

-   Subscription  
    
    表示可清理资源对象，由 Observable 执行之后产生的  

-   Subject  
    
    Subject 是一个特殊的 Observable，更像一个 EventEmitter，它既可以是被观察者/生产者也可以是观察者/消费者  
    |Subject类型|作用|其他|
    |-|-|-
    |BehaviorSubject|继承自Subject，具有存储当前值的特征|存储特点
    |ReplaySubject|ReplaySubject可以将旧数据发送给新的订阅者，这点很像是BehaviorSubject，但是它还有一个额外的特性，它可以记录一部分的observable执行，所以它可以存储多个旧值并发送给它的新订阅者|可以指定要存储多少值以及要存储多长时间
    |AsyncSubject|AsyncSubject是一个Subject变体,其中仅Observable执行的最后一个值发送到其订阅者，并且仅在执行完成时发送|-|
    |Subject|-|-|

-   Operator

    Operator（操作符/算子）本质上是一个纯函数 (pure function)，它接收一个 Observable 作为输入，并生成一个新的 Observable 作为输出,当调用时，它们不会改变现有的Observable。相反，它们返回一个新的 Observable，其订阅逻辑基于第一个Observable。存在用于不同目的的算子，它们可以被分类为：创建，转换，过滤，组合，多播，错误处理，工具等，还有自定义算子。
   

### 应用示例

    JavaScript

### 场景应用

- 串行/并行数据请求
- 切换数据
- 竟态条件