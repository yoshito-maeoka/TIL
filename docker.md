#docker

## run bash
docker exec -it ___IMAGE_ID___ /bin/bash

## run stopped container

1. list all containers even they stopped
```
docker ps -a
484542e0d1a2 7d75b95648f2 "/bin/sh -c 'echo" 24 seconds ago Exited (127) 22 seconds ago focused_heisenberg
```

2. give a name for the stopped container
```
docker commit 484542e0d1a2 debug-target
```

3. run the stopped container with name via it option
```
docker run --rm -it debug-target /bin/bash
```