## Java Memory Model
**Heap**
![enter image description here](https://i0.wp.com/javahonk.com/wp-content/uploads/2014/04/JVM_Structure.png)

For example:
```
Student std = new Student();
```
after executing the line above memory status will be like this.

-   Heap: stores "new Student()"
-   Stack: stores information about "std"
-   Perm Space: stores information about Student class
