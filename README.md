# cod-local 

HBase and Phoenix running in a local container.

Allows emulating the basic functionality of Cloudera Operational Database for local testing and development. 

IMPORTANT: This is a Docker image with temporary local storage, do not use this for Production - YOU WILL HAVE DATA LOSS.

# Running

```
$ docker pull josiahgoodson/cod-local
$ docker run -d -p 8765:8765 josiahgoodson/cod-local
```

You can then connect to Phoenix at http://localhost:8765/

# Thanks

[Francis Chuang](https://github.com/F21) - this is an modified version of his [hbase-phoenix-all-in-one](https://github.com/Boostport/hbase-phoenix-all-in-one)
