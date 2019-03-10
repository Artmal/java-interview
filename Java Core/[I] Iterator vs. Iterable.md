## Iterator vs. Iterable
If collection is **iterable**, then it can be iterated using an iterator(and consequently can be used in a for each loop). 
```
public interface Iterable<T>
{
    Iterator<T> iterator();
}
```

An **Iterator** is the object with iteration state. It lets you check if it has more elements using hasNext() and move to the next element(if any) using next().
```
public interface Iterator<E>
{
    boolean hasNext();
    E next();
    void remove();
}
```
