## What are the difference between programmatic and declarative transaction management?
**Programmatic Transaction Management**

 1. Allows you to manage transactions through programming in your source code.
 2. This means hardcoding transaction logic between your business logic.
 3. Yo use programming to manage transactions.
 4. Flexible, but difficult to maintain with large amount of business logic. Introduces boilerplate between business logic.
 5. Preferred when relative less transaction logic is to be introduced.

**Declarative Transaction Management**

 1. Allows you to manage transactions through configuration.
 2. This means separating transaction logic with business logic.
 3. You use annotations(Or XML files) to manage transactions.
 4. Easy to maintain. Boilerplate is kept away from business logic.
 5. Preferred when working with large amount of Transaction logic.
