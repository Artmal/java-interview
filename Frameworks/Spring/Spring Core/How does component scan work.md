## How does @ComponentScan work?

> `@ComponentScan` will give you a list of all the classes with the `@Component` annotation in a package (or `@Service`/`@Repository`). To do this I imagine they use reflection to enumerate all the classes in a package and find the ones with that annotation.
>
> However according to [other StackOverflow answers](https://stackoverflow.com/questions/520328/can-you-find-all-classes-in-a-package-using-reflection) you can not reliably enumerate all the classes in a package due to how the `ClassLoader`works. So how does `@ComponentScan` seemingly manage to accomplish this?

`@ComponentScan` works differently. Workflow is put shortly this:

-   Find all .class files in same folder and all subfolders
-   Read .class file and wrap it into `Resource` object
-   Check if class has annotations that will make it good candidate
-   If class is good candidate, create bean from it.
