# Splunk Search Queries - Sample and Explanations

This document contains some sample Splunk search queries along with explanations to help you better understand how to use them for different purposes.

---

## 1. Basic Search Queries

### a) Search All Logs 
```spl 
*
### b) Search specific hosts and logs

source="webserver.log" host="HacksProb" sourcetype="main"

### c) Search All Logs with "error"
```spl
index=* sourcetype=*
| search "error"
| table _time, host, sourcetype, message

