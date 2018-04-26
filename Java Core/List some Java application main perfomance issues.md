## List some Java performance issues
1. **Database**
	1. Eager loading everywhere using JPA.
	2. Avoid using cache.
	3. Pool size. 
		Not enough connections make business transactions to wait and the database is under-utilized. On the other hand, too many connections cause bigger response time and database overload. In order to solve this problem you must check whether your application is waiting for a new connection or for a database query to be executed. You can always avoid it though, by optimising the database, test the application with different pool size to check which one fits the case.
2. **Memory**
3. **Concurrency**
	1. Deadlock.
	2. Thread pool size.
	3. Thread grid locks.
		

