## How Group By works?
Group BY groups rows sharing a property so that an aggregate function( AVG, COUNT, MIN, MAX, SUM)  can be applied to each group.

Unfortunately, some SQL Implementations allow GROUP BY  _without_  an aggregate function1.

In this case the result is "not defined / implementation defined" - see the specific implementation documentation to see if it provides any guarantees. 

For increased compatibility and predictable results,  **_use an aggregate function_** _for every field which is not covered by the GROUP BY_  -  _even if_  the particular SQL/RDBMS does not enforce or "require" the use aggregates.
