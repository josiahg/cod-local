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

# Building

Set HBase and Phoenix version env variables
```
$ export HBASE=2.0.0
$ export PHOENIX=5.0.0
```

Clone and build

```
$ git clone https://github.com/josiahg/cod-local
$ cd cod-local
$ docker build . --build-arg HBASE_VERSION=$HBASE --build-arg PHOENIX_VERSION=$PHOENIX -t josiahgoodson/cod-local:latest
```

# Thanks

[Francis Chuang](https://github.com/F21) - this is a modified version of his [hbase-phoenix-all-in-one](https://github.com/Boostport/hbase-phoenix-all-in-one)
