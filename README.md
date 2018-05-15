I did some tuning of payment processing. 


#### 1)This pool NEEDS net_budget to be configured for a value ore than 900 because of coin daemon multiple connections
================================================================================================================

``
sysctl -w net.core.net_budget=900
``

#### 2)Also you HAVE to setup coin daemon for a multithreading, default values are low
``
rcpthreads=300
rpcworkqueue=128
``


#### 3) Start the portal by using forever

```bash
forever init.js
```

