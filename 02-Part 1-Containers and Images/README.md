# Running Containers
- Docker creates virtual environment called containers. Containers run a single process, which can be run in various ways.

## CLI References
- Docker command line (https://docs.docker.com/engine/reference/commandline/cli/ Estimated reading time: 17 minutes) 
```
docker
```
- Container commands (https://docs.docker.com/engine/reference/commandline/container/)
```
docker container COMMAND
```

- docker run (https://docs.docker.com/engine/reference/commandline/run/)
```
docker run [OPTIONS] IMAGE [COMMAND] [ARG...]
``` 
The Docker command line sends instructions to the Docker API. 
The  commands are grouped by object type(such as container or network)
```
docker
docker container --help
docker container run --help
```