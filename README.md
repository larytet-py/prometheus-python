# prometheus-python


This package is similar to https://github.com/larytet-go/prometheus-golang

Given a structure 

```Python
class Statistics {
  def __init__(self):
	  self.ticker = 0
	  self.hits = 0  
	  self.hitApi = 0
	  self.status5xx = 0
}
```

Call to PrometheusStructure() returns

	HELP ticker 1s tick implemented in the code
	TYPE ticker counter
	ticker 0
	HELP hits Count of hits of the HTTP server, includes debug interfaces
	TYPE hits counter
	hits 1
	HELP hitApi 
	TYPE hitApi counter
	hitApi 0
	HELP status5xx 
	TYPE status5xx counter
	status5xx 0

which is accidentally what Prometheus would generate 

You can also initialize a structure of Prometheus counters 

