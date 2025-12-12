---
layout: default
---

![version](https://img.shields.io/badge/version-20%2B-E23089)
![platform](https://img.shields.io/static/v1?label=platform&message=mac-intel%20|%20mac-arm%20|%20win-64&color=blue)
[![license](https://img.shields.io/github/license/miyako/procs)](LICENSE)
![downloads](https://img.shields.io/github/downloads/miyako/procs/total)

# Use procs from 4D

```4d
#DECLARE($params : Object)

If (Count parameters=0)
    
    //execute in a worker to process callbacks
    CALL WORKER(1; Current method name; {})
    
Else 
    
    var $tcp : cs.tcp
    $tcp:=cs.tcp.new()
    $tcp.check({port: 8080}; Formula(onResponse))
    
End if 
```
