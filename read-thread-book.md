book: 图解Java多线程设计模式


- 1章节
	`单例模式
	synchronized`
- 2章节
	`Immutable模式(即实例一旦创建完毕，其内容不可更改模式------联想一下String不可变？)	`
	CopyOnWriteArrayList
	synchronizedList
- 3章节
	`Guarded Suspension模式(实例进入目标之前，防止线程继续执行的模式-----可以防止实例不一致)	`
	阻塞队列LinkedBlockingQueue
- 4章节
 ` Balking模式(如果实例未进入目标状态，则中断方法执行的模式----可防止执行无效的等待和多余的方法)`
- 5章节
	`Producer-Consumer模式(多个爱你成可以协调运行---采用该模式，生成数据的线程与使用的线程在并发运行时不会互相抢占)	`
	ArrayBlockingQueue
- 6章节
	`Read-Write-Lock 模式(互斥处理---该模式，写数据的线程只能有一个，但读数据的线程可以有很多，可以提高程序的整体性能)`
	ReentrantReadWriteLock
- 7章节
  `Thread-Per-Message模式(委托给其他线程---线程可以将任务委托给其他线程，自己则直接处理接下来的工作，能够提高程序的响应性)`
	Executor和ExectorService

- 8章节
	`Worker Thread模式(多个线程通过线程池进行等待，然后按照顺序接受工作并执行---可以减少创建线线程的资源消耗，可以调节等待线程的个数来控制可用的资源)`
	AWT及SwingJFC的线程处理方法，
- 9章节
	`Future模式(可以同步获取交给其他任务的结果---适用于调用异步方法的情况)`
	Future、FutureTask、Callable
- 10章节
	`Two Phase Termination模式(能够采用合适的终止处理来安全地终止线程----中断处理)`
	CountDownLatch、CylicBarrier
- 11章节
	`Thread-Specific Storage模式(每个线程都会有自己的变量空间----多个线程之间的变量空间是完全隔离的，所以不需要执行互斥处理)`
	ThreadLocal类的使用方法

- 12章节
	`Active Object模式(程序会创建主动对象---主动对象将接受外部消息，并交给自己的线程来处理------方法调用和方法执行时彼此分开的)`
- 13章节
	`总结`
