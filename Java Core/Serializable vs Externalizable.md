## Serializable vs Externalizable
By implementating `java.io.Serializable`, you get "automatic" serialization capability for objects of your class. No need to implement any other logic, it'll just work. The Java runtime will use reflection to figure out how to marshal and unmarshal your objects.

In earlier version of Java, reflection was very slow, and so serializaing large object graphs (e.g. in client-server RMI applications) was a bit of a performance problem. To handle this situation, the `java.io.Externalizable` interface was provided, which is like `java.io.Serializable` but with custom-written mechanisms to perform the marshalling and unmarshalling functions (you need to implement `readExternal` and `writeExternal` methods on your class). This gives you the means to get around the reflection performance bottleneck.

A big downside of `Externalizable` is that you have to maintain this logic yourself - if you add, remove or change a field in your class, you have to change your `writeExternal`/`readExternal` methods to account for it.

In summary, `Externalizable` is a relic of the Java 1.1 days. There's really no need for it any more.
