## Transaction isolation levels
1. READ UNCOMMITTED(Dirty read)
Data is available right after query(even we didn't do a commit yet).
2. READ COMMITTED
Data is available only after transaction's commit.
3. REPEATABLE READ(**MySQL Default**)
Begin transaction
Read Data
*Another transaction commit's some changes to data which transaction works with *
Read Data - Same data as before
New records from other transactions will be visible though.
4. SERIALIZABLE
No one can even add new row into database when transaction is running(except the transaction, of course).

