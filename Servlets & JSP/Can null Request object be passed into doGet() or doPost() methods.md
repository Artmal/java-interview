## Can null Request object be passed to doGet() or doPost() methods?

Yes, if we propogate null value in filter: `chain.doFilter(null, response)`
