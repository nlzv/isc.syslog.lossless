SYSLOG facility in ISC cache is cyclic buffer etries so when
it is filled up then a new entry overwrites old.
Since it is important information about OS errors or key errors in cache kernel
it is might desirable to holds this info during longer time than overwriting starts happens.

^%z.syslog utility relogs SYSLOG info into a file or global and can be stared as daemon
as COS job command for example SYSTEM^%ZSTART,SYSTEM^%ZSTOP or as system task.
For details see comment before routine label.
It is expected to load it and compile into %SYS namespace.

Note: it is not tested for big endean cache kernel.





