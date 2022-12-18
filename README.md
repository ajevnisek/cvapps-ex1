# Computer Vision Exercise #1 Environment

This is a basic dockerfile.


# Setup
Create a directory shared with the docker

# Build docker Image
```bash
docker image build -t ajevnisek/cvapps-ex1 .
```

# Run docker Container
```bash
docker run --name ex1-ex1-docker-demo -dit ajevnisek/cvapps-ex1 sleep infinity
```

## Watch dockers list:
```bash
docker container ls
```

## Kill docker Container:
```bash
docker kill <docker-id>
```

## Debug
### watch logs
```bash
docker logs ex1-docker-demo -f
```

### bash to the container
```bash
docker exec -it ex1-docker-demo bash
```


# Misc

Push docker to `docker.io`:
```bash
docker push ajevnisek/cvapps-ex1:latest
```

Clear all docker cache:
```bash
docker system prune -a
```

# Run this image with run:ai:
```bash
runai submit -g 1 --name base-ex1-docker-demo -i ajevnisek/cvapps-ex1:latest --pvc=storage:/storage
```
