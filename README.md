# docker_rust
Docker container for rust development.  This container runs commands as the user used to build the image (i.e. the current user at image build time) instead of the root user.

### Create the container with

```
UID=$(id -u) GID=$(id -g) docker compose up -d
```
or maybe
```
UID=$(id -u) GID=$(id -g) docker-compose up -d
```
for older versions of docker.

### Recreate the container with

```
UID=$(id -u) GID=$(id -g) docker compose up -d --build
```
_I won't mention the `docker-compose` versions anymore, but you get the idea._ :)

### Connect to the container to execute Rust/Cargo commands

```
docker exec -it rust-dev /usr/bin/zsh
```

