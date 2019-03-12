## wait() vs. sleep()
**wait()** is an instance method that's used for thread syncronization.

It can be called on any object, as it's defined right on java.lang.Object, but it can only be called from a syncrhonized block. It releases the clock on the object so that another thread can jump in and acuqire a lock. 

On the other hand, **Thread.sleep()** is a static method that can be called from any context. Thread.sleep() pauses the current thread and does not releasy any locks. 
