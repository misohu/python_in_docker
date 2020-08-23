Get the python image: 
```
docker pull python:3.8-slim
``` 

Get all the local images:
```
docker image ls 
```

Run python image locally 
```
docker run python:3.8-slim
```

Run python image locally for ever: 
```
docker run -t -d python:3.8-slim
```

List running containers:
```
docker ps
```

Get to the bash of the running container:
```
docker exec -ti <containerId> bash
```

Cmd + D to leave the container. Stop the running container:
```
docker stop <containerId>
```

Run container with the name:
```
docker run -t -d --name="jupyter"
```

Remove exited container
```
docker rm <containerId>
```

Remove container on exit 
```
docker run -rm -t -d --name="jupyter"
```

Commit changes in container
```
docker commit <containerId> <newImageId>
````

Run the jupyter in the container:
```
jupyter lab --ip='0.0.0.0' --port=8888 --no-browser --allow-root
```

Run container with bound ports
```
docker run --rm -t -d --name=jupyter -p 8888:8888 <imageId>
```

Run container with bind volume 
```
 docker run --rm -t -d --name=jupyter -p 8888:8888 --mount src="$(pwd)",target=/app,type=bind jupter_v2:latest
```

