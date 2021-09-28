# index

## Thread

通过继承Thread的方式，可以创建一个线程，需要重写其中的run方法，启动线程时，通过调用start方法启动。形如：

```java
new MyThread().start();
```

## Runnable

通过实现Runnable接口的方式，可以创建一个线程，需要重写其中的run方法，启动线程时，将自定义类的实例作为一个参数，调用Thread的构造方法，得到一个线程实例，再调用start方法启动。形如：

```java
new Thread(new MyRunnable()).start();
```

## Callable

通过实现callable接口的方式，可以创建一个线程，需要重写其中的call方法。启动线程时，需要新建一个Callable的实例，再用FutureTask实例包装它，最终，再包装成Thread实例，调用start方法启动，并且，可以通过FutureTask的get方法来获取返回值。形如：

## ExecutorService线程池

ExecutorService.new...

## Executor

## Future

Future就是对于具体的Runnable或者Callable任务的执行结果进行取消、查询是否完成、获取结果。必要时可以通过get方法获取执行结果，该方法会阻塞直到任务返回结果。

## FutureTask

Future接口的具体实现，它既可以作为Runnable被线程执行，又可以作为Future得到Callable的返回值。

