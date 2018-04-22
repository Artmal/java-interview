## Tell us about CopyOnWriteArrayList
It's a class from java.util.concurrent package which allows s to iterate over a list in a thread-safe way without an explicit synchronization.

The design of the CopyOnWriteArrayList uses an interesting technique to make it thread-safe without a need for synchronization. When we are using any of the modify methods - such as add() or remove() - the whole content of the CopyOnWriteArrayList is copied into the new internal copy.

Due to this simple fact, we can iterate over the list in a safe way, even when concurrent modification is happening.

Iterator of CopyOnWriteArrayList is fail-safe and doesn't throw ConcurrentModificationException even if underlying CopyOnWriteArrayList is modified once Iteration begins because iterator is operating on separate copy of ArrayList. Consequently all the updated made on CopyOnWriteArrayList is not available to Iterator.

To get the most updated version do a new read like list.iterator().



