## BigInteger & BigDecimal
**BigInteger**
Long is not enough? How about  a BigInteger which is represented as an int[] of digits? You can have INTEGER.MAX_VALUE digits!
___
**BigDecimal**
Float and double primitive types are not suitable for money related operation and high-precision calculations.

Use BigDecimal for this!
The unscaled value of the [BigDecimal](http://www.docjar.com/html/api/java/math/BigDecimal.java.html) is stored in a [BigInteger](http://www.docjar.com/html/api/java/math/BigInteger.java.html). The [precision and scale](http://en.wikipedia.org/wiki/Significant_figures) are stored separately in integer fields:

 ```
BigInteger intVal
int scale
int precision
```
