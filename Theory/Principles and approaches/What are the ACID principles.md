## What are ACID principles?
In computer science ACID is a set of properties of database transactions intended to guarantee validity even in the event of errors, power failures, etc.

In the context of databases a sequence of database operations that satisfies the ACID properties, and thus can be perceived as a single logical operation on the data, is called a transaction

**Atomicity**   
In a transaction involving two or more discrete pieces of information, either all of the pieces are committed or none are.

**Consistency**  
Consistent = transaction won't violate declared system integrity constraints

**Isolation**  
A transaction in process and not yet committed must remain isolated from any other transaction.

**Durability**  
Committed data is saved by the system such that, even in the event of a failure and system restart, the data is available in its correct state.

 
