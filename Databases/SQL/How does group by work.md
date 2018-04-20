## How Group By works?
The GROUP BY statement is often used with aggregate functions (COUNT, MAX, MIN, SUM, AVG) to group the result-set by one or more columns.

Suppose you have the following tables:
Users
|ID| username |
|--|--|
| 1 | Artmal |
| 2 | Travian boy|
| 3 | Lagger |

User Roles
|user_id| role |
|--|--|
| 1 | Admin |
| 2 | User |
| 3 | User |

Count the amount of each role.

Answer:
SELECT ur.role, COUNT(ur.role) FROM user_roles ur INNER JOIN users ON ur.user_id = users.id GROUP BY ur.role;
