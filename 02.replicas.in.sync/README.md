# 02 When Replicas are Not in Sync

## Prerequisites
1. Docker
2. New Relic Account with an Ingest license key

## Demo Setup & Shutdown
### Start
```docker compose up -d```
### End
```docker compose down -v```

The ```-v``` is important since the Kafka images create volumes to store the messages and you do not want to reuse them across docker runs.

## Demos
### 00 Setup
http://localhost:8888/lab/tree/work/00%20Setup.ipynb
### 01 Bursty Traffic
http://localhost:8888/lab/tree/work/01%20Bursty%20Traffic.ipynb
### 02 Broker Failure
http://localhost:8888/lab/tree/work/02%20Broker%20Failure.ipynb
### 03 Transient Network Errors
http://localhost:8888/lab/tree/work/03%20Transient%20Network%20Errors.ipynb


## Caveats
- If your local machine is not powerful enough to run the 5 docker containers, you may get skewed results
- If the docker container's disk gets full, you may get errors that do not directly correlate to a disk issue.
- The Jupyter notebook uses Kafka 3.7 while the docker images use Apache's Kafka image with the ```latest``` tag. Do with that what you will.