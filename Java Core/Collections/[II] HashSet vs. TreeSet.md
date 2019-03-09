## HashSet vs. TreeSet
Both guarantee duplicate-free collection of elements.

**HashSet**

 - the class offers constant time performance for the basic operations(add, remove, contains and size).
 - it does not guarantee that the order of elements will remain constant over time.
 - Allow null values.

**TreeSet**

 - guarantees log(n) time cost for the basic operations(add, remove and contains)
 - Guarantees that elements of set will be sorted(ascending, natural, or the one specific by you via its constructor).

It's generaly faster to add elements to the HashSet and then convert the collection to a TreeSet for a duplicate-free sorted traversal.
