# 每周总结可以写在这里

###  事件循环 (event loop)

#### 事件循环是什么？

事件循环是浏览器执行任务的机制，它会不断循环判断消息队列中是否有任务，队列中的任务都是指宏任务，而宏任务中包含微任务队列，在宏任务结束前后执行微任务队列，知道微任务队列中为空才结束这个宏任务。

#### 消息队列是什么？

消息队列是一种先进先出的数据结构，用于存放要执行的任务。

#### 宏任务是什么？

宏任务是消息队列中的一个task，它可能是由用户交互、资源加载、script、web api（setTimeout, setInterval, setImmediate等）等所产生的。

#### 微任务是什么？

微任务是宏任务中的一个子任务组，在宏任务结束前执行，为什么会有微任务的出现？因为在消息队列中无法根据优先级来执行任务，导致实时性较高的任务无法立即执行，像监听DOM元素的MutationObserve等，Promise.resolve 和 Promise.reject 都会产生一个微任务。微任务中也有可能产生一个微任务，当所以微任务执行完成才会结束当前的宏任务。