## Explain N+1 problem
By default Hibernate has lazy loading enabled. It means that in case of one-to-many relationship we don't get children of the entity by default querying.

**Example**
Suppose we have ***cars*** and ***wheels*** tables. A car can have many wheels and each will belong to particular car(one-to-many relationship).

We want to query cars with specific parameters. Lets say we want to get all "Mercedes" cars.

    SELECT * FROM cars WHERE manufacturer="Mercedes"

We get our cars and we want to print information about all wheels of all cars. But we don't have them! We need to fire another **n** quiries to get them. 
