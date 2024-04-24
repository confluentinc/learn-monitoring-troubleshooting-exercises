# 02 When Replicas Are Not in Sync

## Prerequisites
1. Docker
2. New Relic Account with an Ingest license key
    - While there, create a new dashboard by importing the json definition in this repo.

## Demo Setup & Shutdown
### Start
```docker compose up -d```
### End
```docker compose down -v```


The ```-v``` is important since the Kafka images create volumes to store the messages and you do not want to reuse them across container runs.

## Demos
### 00 Setup
http://localhost:8888/lab/tree/work/00%20Setup.ipynb
### 01 Broker Failure
http://localhost:8888/lab/tree/work/01%20Broker%20Failure.ipynb
### 02 Transient Network Errors
http://localhost:8888/lab/tree/work/02%20Transient%20Network%20Errors.ipynb


## Caveats
- If your local machine is not powerful enough to run the 5 Docker containers, you may get skewed results
- If the Docker container's disk gets full, you may get errors that do not directly correlate to a disk issue.
- The Jupyter notebook uses Kafka 3.7 while the Docker images use Apache's Kafka image with the ```latest``` tag. Do with that what you will.