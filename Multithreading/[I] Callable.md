## Callable 
-   A `Callable` needs to implement `call()` method while a `Runnable` needs to implement `run()` method.
-   A `Callable` can return a value but a `Runnable` cannot.
-   A `Callable` can throw checked exception but a `Runnable` cannot.
-   A `Callable` can be used with `ExecutorService#invokeXXX(Collection<? extends Callable<T>> tasks)` methods but a `Runnable` cannot be.
