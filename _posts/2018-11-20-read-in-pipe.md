---
layout: post
---
- if a process open a read pipe and use read function to read data. If on the other side, there is a write pipe opened but doesn't have data write in, the read function will be blocked to wait for data. But if there is `NO` write pipe opened on the other side, the read function will receive `0`(indicating like an end of file).
ps: if the file descriptor is invalid, the return value of the read function will be `-1`. 
