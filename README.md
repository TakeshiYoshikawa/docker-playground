# docker-playground

## How to Build
1. Firstly, you need to install Docker on [Official website](https://www.docker.com/).

2. After you have installed and start up Docker, open cmd or Docker application and run
```
docker-compose build
```

## How to Start
To start each service individually, run:
```
docker-compose up -d mongo
docker-compose up -d app
docker-compose up -d client
```

Or if you want to start all at the same time, run:
```
docker-compose up
```


## Check container status
Run `docker ps` and check if all CONTAINER IDs are present like that:
```
CONTAINER ID   IMAGE                      COMMAND                  CREATED          STATUS          PORTS                      NAMES
f2701459b14f   docker-playground-client   "docker-entrypoint.s…"   5 seconds ago    Up 5 seconds    0.0.0.0:3000->3000/tcp     client
1fbe5a70156f   docker-playground-app      "docker-entrypoint.s…"   16 seconds ago   Up 15 seconds   0.0.0.0:4000->4000/tcp     app
b38fe4ae28a2   mongo                      "docker-entrypoint.s…"   27 seconds ago   Up 27 seconds   0.0.0.0:27017->27017/tcp   mongo
```

## How to stop
Simply run:
```
docker-compose stop
```