# docker_rust
Docker container for rust development

###Create the container with

```
docker compose up -d
```
or maybe
```
docker-compose up -d
```
for older versions of docker.

###Recreate the container with

```
docker compose up -d --build
```
_I won't mention the `docker-compose` versions anymore, but you get the idea._ :)

###Connect to the container to execute Rust/Cargo commands

```
docker exec -it docker_rust-dev-1 /bin/bash
```
_Your container name may vary based on your repository folder name, but it should be easy to figure out with `docker ps`._
