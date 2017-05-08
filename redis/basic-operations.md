
# Redis Basic Operations


```
set name Batur
get name  // "Batur"
expire name 10
get name // after 10 seconds, nil
flushall // delete all keys
select 5 // select the 6th database, and by default there are 16 databases.
```