## WeakHashMap
The WeakHashMap is a hashtable-based implementation of the Map interface, with keys are of a WeakReference type.

An entry in a WeakHashMap will automatically be removed when its key is no longer ordinary use, meaning that there is no single reference that point to that key. 

The data structure can be used for custom cache implementation. BTW, creating your own cache implementation is almost always a bad idea.
