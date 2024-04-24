# 02 When Replicas Are Not in Sync

## Prerequisites
1. Docker
    -  Install [Docker Desktop](https://docs.docker.com/desktop/) (version 4.27.2 or later) or [Docker Engine](https://docs.docker.com/engine/install/) (version 25.0.3 or later) if you don’t already have it
    - Install the [Docker Compose plugin](https://docs.docker.com/compose/install/) if you don’t already have it. This isn’t necessary if you have Docker Desktop since it includes Docker Compose.
    - Start Docker if it’s not already running, either by starting Docker Desktop or, if you manage Docker Engine with systemd, via systemctl
    - Verify that Docker is set up properly by ensuring no errors are output when you run ```docker info``` and ```docker compose version``` on the command line
2. New Relic Account with an Ingest license key
    - While there, create a new dashboard by importing the json definition in this repo.

## Demo Setup & Shutdown
### Start
```
docker compose up -d
```
### End
```
docker compose down -v
```


The ```-v``` is important since the Kafka images create volumes to store the messages and you do not want to reuse them across container runs.

## Demos
00. [Setup](http://localhost:8888/lab/tree/work/00%20Setup.ipynb)
90. [Broker Failure](http://localhost:8888/lab/tree/work/01%20Broker%20Failure.ipynb)
00. [Transient Network Errors](http://localhost:8888/lab/tree/work/02%20Transient%20Network%20Errors.ipynb)


## Caveats
- If your local machine is not powerful enough to run the 5 Docker containers, you may get skewed results
- If the Docker container's disk gets full, you may get errors that do not directly correlate to a disk issue.
- The Jupyter notebook uses Kafka 3.7 while the Docker images use Apache's Kafka image with the ```latest``` tag. Do with that what you will.