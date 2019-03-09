## Provide an example of using Reflection API
Most  use cases for this occur in "frameworky" environments. Think about JUnit, for example, that wants to execute all methods that are annotated with @Test. Once it found them with a class path scan it uses getMethod() and invoke() to call them.

Spring and other web frameworks act similarly when looking for controllers and request mappings. 
