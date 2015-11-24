SYSLOG facility of ISC cache are entries in cyclic buffer so when
it is filled up then a new entries overwrite old.<br/>
Since it is important information about OS errors or key errors in cache kernel
it might be desirable to hold this info during longer time than overwriting starts to happen.<br/>

^%z.syslog utility relogs SYSLOG info into a file or global and can be stared as daemon
as COS job command for example SYSTEM^%ZSTART or as system task.
```
SYSTEM^%ZSTART
 D relog^%z.syslog("file:"_$zu(12)_"sys.log",1)
```

For details see comment before routine label.<br/>
It is expected to load it and compile into %SYS namespace.<br/>

Note: it is not tested for big endean cache kernel.





