## Optimistic vs pessimistic locks
Transactional isolation is usually implemented by locking whatever is accessed in a transaction. There are two different approaches to transactional locking: pessimistic locking and optimistic locking.

**Pessimistic locking**
Resource is locked from the time is is first accessed in a transaction until the transaction is finished, making it inaccessible to other transaction during that time. 

In the banking application example, an account is locked as soon as it is accessed in a transaction. Attempts to use the account in other transaction while it is locked will either result in the other process being delayed until the account lock is released, or that the process transaction will be rolled back. The lock exists until the transaction hsa either been committed or rolled back.

**Optimistic locking**
Resource is not actually locked when it is first is accessed by a transaction. Instead, the state of the resource at the time when it would have been locked with the pessimistic locking approach is saved. 

At commit time, when the resource is about to be updated in persistent storage, the state of the resource is read from storage again and compared to the state that was saved when the resource was first accessed in the transaction.
