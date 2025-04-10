## 多进程
1. 创建多进程`p = multiprocessing.Process(target=func)`
2. 开始任务`p.start()`
3. 父进程等待子进程结束`p.join()`
4. 进程间通信使用`multiprocessing.Queue`，最好使用单向队列避免自己收到自己发的消息，Queue实例可以通过创建进程时参数传递给子进程，`Queue.put/get`来发送接收
