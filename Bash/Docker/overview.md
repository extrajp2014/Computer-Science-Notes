## Container Management

| Code | Description |
|------|-------------|
| `docker run [OPTIONS] IMAGE [COMMAND] [ARG...]` | Creates and starts a new container from an image. |
| `docker run -d IMAGE` | Runs a container in detached (background) mode. |
| `docker run -it IMAGE` | Runs a container interactively with a pseudo-TTY. |
| `docker run --name mycontainer IMAGE` | Runs a container with a custom name. |
| `docker run -p 8080:80 IMAGE` | Runs a container with port mapping (host:container). |
| `docker run -v /host/path:/container/path IMAGE` | Runs a container with a volume mount. |
| `docker run -e VAR=value IMAGE` | Runs a container with an environment variable. |
| `docker run --env-file .env IMAGE` | Runs a container with environment variables from a file. |
| `docker run --network mynetwork IMAGE` | Runs a container connected to a specific network. |
| `docker run --restart=always IMAGE` | Runs a container with a restart policy. |
| `docker run --rm IMAGE` | Runs a container and automatically removes it when it exits. |
| `docker run --read-only IMAGE` | Runs a container with a read-only filesystem. |
| `docker run --tmpfs /tmp IMAGE` | Runs a container with a tmpfs mount. |
| `docker run --cpus=2 IMAGE` | Runs a container with CPU limits. |
| `docker run --memory=512m IMAGE` | Runs a container with memory limits. |
| `docker run --gpus all IMAGE` | Runs a container with GPU access. |
| `docker run --user user:group IMAGE` | Runs a container as a specific user. |
| `docker run --workdir /path IMAGE` | Runs a container with a custom working directory. |
| `docker run --dns 8.8.8.8 IMAGE` | Runs a container with custom DNS servers. |
| `docker run --dns-search example.com IMAGE` | Runs a container with custom DNS search domains. |
| `docker run --hostname myhost IMAGE` | Runs a container with a custom hostname. |
| `docker run --mac-address MAC IMAGE` | Runs a container with a custom MAC address. |
| `docker run --privileged IMAGE` | Runs a container with extended privileges. |
| `docker run --cap-add=CAP IMAGE` | Runs a container with additional Linux capabilities. |
| `docker run --cap-drop=CAP IMAGE` | Runs a container with dropped Linux capabilities. |
| `docker run --security-opt seccomp=profile.json IMAGE` | Runs a container with security options. |
| `docker run --ulimit nofile=1024:1024 IMAGE` | Runs a container with ulimit settings. |
| `docker run --sysctl net.ipv4.ip_forward=1 IMAGE` | Runs a container with kernel parameters. |
| `docker start [OPTIONS] CONTAINER [CONTAINER...]` | Starts one or more stopped containers. |
| `docker start -a CONTAINER` | Starts a container and attaches to it. |
| `docker start --checkpoint=checkpoint CONTAINER` | Starts a container from a checkpoint. |
| `docker stop [OPTIONS] CONTAINER [CONTAINER...]` | Stops one or more running containers. |
| `docker stop -t 30 CONTAINER` | Stops a container with a timeout of 30 seconds. |
| `docker restart [OPTIONS] CONTAINER [CONTAINER...]` | Restarts one or more containers. |
| `docker restart -t 30 CONTAINER` | Restarts a container with a timeout of 30 seconds. |
| `docker pause CONTAINER [CONTAINER...]` | Pauses one or more containers. |
| `docker unpause CONTAINER [CONTAINER...]` | Unpauses one or more containers. |
| `docker rm [OPTIONS] CONTAINER [CONTAINER...]` | Removes one or more containers. |
| `docker rm -f CONTAINER` | Force removes a running container. |
| `docker rm -v CONTAINER` | Removes a container and its associated volumes. |
| `docker rm $(docker ps -aq)` | Removes all stopped containers. |
| `docker ps [OPTIONS]` | Lists containers. |
| `docker ps -a` | Lists all containers (including stopped ones). |
| `docker ps -q` | Lists only container IDs. |
| `docker ps --filter "status=exited"` | Lists containers filtered by status. |
| `docker ps --format "{{.ID}}: {{.Image}}"` | Lists containers with a custom format. |
| `docker ps --no-trunc` | Lists containers without truncating output. |
| `docker inspect [OPTIONS] NAME|ID [NAME|ID...]` | Returns low-level information about containers, images, or tasks. |
| `docker inspect --format='{{.NetworkSettings.IPAddress}}' CONTAINER` | Inspects a container and formats the output. |
| `docker inspect --type container CONTAINER` | Inspects a container. |
| `docker inspect --type image IMAGE` | Inspects an image. |
| `docker inspect --type task TASK` | Inspects a task. |
| `docker logs [OPTIONS] CONTAINER` | Fetches the logs of a container. |
| `docker logs -f CONTAINER` | Follows the logs of a container. |
| `docker logs --since 1h CONTAINER` | Shows logs from the last hour. |
| `docker logs --tail 100 CONTAINER` | Shows the last 100 lines of logs. |
| `docker logs -t CONTAINER` | Shows logs with timestamps. |
| `docker exec [OPTIONS] CONTAINER COMMAND [ARG...]` | Runs a command in a running container. |
| `docker exec -it CONTAINER bash` | Starts an interactive shell in a running container. |
| `docker exec -u user:group CONTAINER COMMAND` | Runs a command as a specific user in a container. |
| `docker exec -w /path CONTAINER COMMAND` | Runs a command in a specific working directory. |
| `docker exec -e VAR=value CONTAINER COMMAND` | Runs a command with environment variables. |
| `docker attach [OPTIONS] CONTAINER` | Attaches to a running container. |
| `docker attach --sig-proxy=true CONTAINER` | Attaches to a container and proxies signals. |
| `docker wait CONTAINER [CONTAINER...]` | Blocks until one or more containers stop, then prints their exit codes. |
| `docker kill [OPTIONS] CONTAINER [CONTAINER...]` | Kills one or more running containers. |
| `docker kill -s SIGTERM CONTAINER` | Kills a container with a specific signal. |
| `docker commit [OPTIONS] CONTAINER [REPOSITORY[:TAG]]` | Creates a new image from a container's changes. |
| `docker commit -a author -m message CONTAINER REPO:TAG` | Commits a container with author and message. |
| `docker cp [OPTIONS] CONTAINER:SRC_PATH DEST_PATH|-` | Copies files/folders between a container and the local filesystem. |
| `docker cp CONTAINER:/path/to/file /host/path` | Copies a file from a container to the host. |
| `docker cp /host/path/file CONTAINER:/path/to/dest` | Copies a file from the host to a container. |
| `docker diff CONTAINER` | Inspects changes on a container's filesystem. |
| `docker export [OPTIONS] CONTAINER` | Exports a container's filesystem as a tar archive. |
| `docker export -o file.tar CONTAINER` | Exports a container to a tar file. |
| `docker port CONTAINER [PRIVATE_PORT[/PROTO]]` | Lists the public-facing port that is NAT'd to PRIVATE_PORT. |
| `docker rename CONTAINER NEW_NAME` | Renames a container. |
| `docker update [OPTIONS] CONTAINER [CONTAINER...]` | Updates configuration of one or more containers. |
| `docker update --cpus=2 CONTAINER` | Updates CPU limits for a container. |
| `docker update --memory=512m CONTAINER` | Updates memory limits for a container. |
| `docker prune containers` | Removes all stopped containers. |
| `docker prune containers -f` | Force removes all stopped containers without confirmation. |

---
## Image Management

| Code | Description |
|------|-------------|
| `docker images [OPTIONS] [REPOSITORY[:TAG]]` | Lists images. |
| `docker images -a` | Lists all images (including intermediate layers). |
| `docker images --filter "dangling=true"` | Lists dangling images. |
| `docker images --format "{{.ID}}: {{.Repository}} ({{.Tag}})"` | Lists images with a custom format. |
| `docker images --no-trunc` | Lists images without truncating output. |
| `docker pull [OPTIONS] NAME[:TAG|@DIGEST]` | Pulls an image or a repository from a registry. |
| `docker pull IMAGE:TAG` | Pulls a specific tag of an image. |
| `docker pull --platform linux/amd64 IMAGE` | Pulls an image for a specific platform. |
| `docker push [OPTIONS] NAME[:TAG]` | Pushes an image or a repository to a registry. |
| `docker push IMAGE:TAG` | Pushes a specific tag of an image. |
| `docker build [OPTIONS] PATH | Builds an image from a Dockerfile. |
| `docker build -t image:tag .` | Builds an image with a tag from the current directory. |
| `docker build -t image:tag -f Dockerfile.custom .` | Builds an image from a custom Dockerfile. |
| `docker build --no-cache -t image:tag .` | Builds an image without using cache. |
| `docker build --build-arg VAR=value -t image:tag .` | Builds an image with build arguments. |
| `docker build --target stage -t image:tag .` | Builds a specific stage from a multi-stage Dockerfile. |
| `docker build --network=host -t image:tag .` | Builds an image with host network mode. |
| `docker build --squash -t image:tag .` | Builds an image and squashes layers into a single layer. |
| `docker buildx build [OPTIONS] PATH` | Builds an image using BuildKit (extended build capabilities). |
| `docker buildx build --platform linux/amd64,linux/arm64 -t image:tag --push .` | Builds a multi-platform image and pushes it. |
| `docker rmi [OPTIONS] IMAGE [IMAGE...]` | Removes one or more images. |
| `docker rmi -f IMAGE` | Force removes an image. |
| `docker rmi $(docker images -q)` | Removes all images. |
| `docker rmi $(docker images -q --filter "dangling=true")` | Removes all dangling images. |
| `docker load [OPTIONS]` | Loads an image from a tar archive or STDIN. |
| `docker load -i image.tar` | Loads an image from a tar file. |
| `docker save [OPTIONS] IMAGE [IMAGE...]` | Saves one or more images to a tar archive (streamed to STDOUT by default). |
| `docker save -o image.tar IMAGE` | Saves an image to a tar file. |
| `docker save IMAGE1 IMAGE2 > images.tar` | Saves multiple images to a tar file. |
| `docker import [OPTIONS] file|URL [REPOSITORY[:TAG]]` | Creates an image from a tarball. |
| `docker tag SOURCE_IMAGE[:TAG] TARGET_IMAGE[:TAG]` | Creates a tag TARGET_IMAGE that refers to SOURCE_IMAGE. |
| `docker tag IMAGE:OLD_TAG IMAGE:NEW_TAG` | Creates a new tag for an existing image. |
| `docker history [OPTIONS] IMAGE` | Shows the history of an image. |
| `docker history --no-trunc IMAGE` | Shows the history of an image without truncating output. |
| `docker inspect IMAGE` | Returns low-level information about an image. |
| `docker prune images` | Removes dangling images. |
| `docker prune images -a` | Removes all images not used by at least one container. |
| `docker prune images -f` | Force removes dangling images without confirmation. |

---
## Network Management

| Code | Description |
|------|-------------|
| `docker network ls [OPTIONS]` | Lists networks. |
| `docker network ls --filter "driver=bridge"` | Lists networks filtered by driver. |
| `docker network create [OPTIONS] NETWORK` | Creates a new network. |
| `docker network create --driver bridge mynetwork` | Creates a new bridge network. |
| `docker network create --driver overlay mynetwork` | Creates a new overlay network. |
| `docker network create --driver host mynetwork` | Creates a new host network. |
| `docker network create --driver none mynetwork` | Creates a new none network. |
| `docker network create --subnet=172.20.0.0/16 mynetwork` | Creates a network with a custom subnet. |
| `docker network create --gateway=172.20.0.1 mynetwork` | Creates a network with a custom gateway. |
| `docker network create --ip-range=172.20.0.0/24 mynetwork` | Creates a network with a custom IP range. |
| `docker network create --attachable mynetwork` | Creates an attachable network. |
| `docker network create --internal mynetwork` | Creates an internal network. |
| `docker network inspect [OPTIONS] NETWORK [NETWORK...]` | Displays detailed information about one or more networks. |
| `docker network connect [OPTIONS] NETWORK CONTAINER` | Connects a container to a network. |
| `docker network connect --alias myalias NETWORK CONTAINER` | Connects a container to a network with an alias. |
| `docker network disconnect [OPTIONS] NETWORK CONTAINER` | Disconnects a container from a network. |
| `docker network disconnect -f NETWORK CONTAINER` | Force disconnects a container from a network. |
| `docker network rm [OPTIONS] NETWORK [NETWORK...]` | Removes one or more networks. |
| `docker network rm NETWORK1 NETWORK2` | Removes multiple networks. |
| `docker network prune [OPTIONS]` | Removes all unused networks. |
| `docker network prune -f` | Force removes all unused networks without confirmation. |

---
## Volume Management

| Code | Description |
|------|-------------|
| `docker volume ls [OPTIONS]` | Lists volumes. |
| `docker volume ls --filter "dangling=true"` | Lists dangling volumes. |
| `docker volume create [OPTIONS] [VOLUME]` | Creates a volume. |
| `docker volume create --driver local myvolume` | Creates a volume with a specific driver. |
| `docker volume create --opt type=nfs --opt o=addr=nfs.example.com,rw myvolume` | Creates an NFS volume. |
| `docker volume create --label mylabel=value myvolume` | Creates a volume with labels. |
| `docker volume inspect [OPTIONS] VOLUME [VOLUME...]` | Displays detailed information about one or more volumes. |
| `docker volume rm [OPTIONS] VOLUME [VOLUME...]` | Removes one or more volumes. |
| `docker volume rm -f VOLUME` | Force removes a volume. |
| `docker volume prune [OPTIONS]` | Removes all unused volumes. |
| `docker volume prune -f` | Force removes all unused volumes without confirmation. |
| `docker volume prune -a` | Removes all volumes not used by at least one container. |

---
## System Management

| Code | Description |
|------|-------------|
| `docker info [OPTIONS]` | Displays system-wide information. |
| `docker version [OPTIONS]` | Shows the Docker version information. |
| `docker version --format '{{.Client.Version}}'` | Shows the Docker client version with a custom format. |
| `docker events [OPTIONS]` | Gets real-time events from the server. |
| `docker events --filter 'event=create'` | Filters events by type. |
| `docker events --filter 'container=CONTAINER'` | Filters events by container. |
| `docker events --filter 'image=IMAGE'` | Filters events by image. |
| `docker events --since 1h` | Shows events from the last hour. |
| `docker stats [OPTIONS] [CONTAINER...]` | Displays a live stream of container(s) resource usage statistics. |
| `docker stats --no-stream` | Displays container resource usage statistics without streaming. |
| `docker stats -a` | Shows all containers (including stopped ones). |
| `docker top CONTAINER [ps OPTIONS]` | Displays the running processes of a container. |
| `docker top -ef CONTAINER` | Displays the running processes of a container with full format. |
| `docker df [OPTIONS]` | Shows disk usage of Docker. |
| `docker df -v` | Shows disk usage with verbose output. |
| `docker system prune [OPTIONS]` | Removes unused data. |
| `docker system prune -a` | Removes all unused containers, networks, images, and volumes. |
| `docker system prune -a -f` | Force removes all unused data without confirmation. |
| `docker system prune --volumes` | Removes unused volumes. |
| `docker system info` | Displays system-wide information (alias for docker info). |

---
## Docker Compose

| Code | Description |
|------|-------------|
| `docker compose up [OPTIONS] [SERVICE...]` | Creates and starts containers for a service. |
| `docker compose up -d` | Creates and starts containers in detached mode. |
| `docker compose up --build` | Builds images before starting containers. |
| `docker compose up --force-recreate` | Force recreates containers. |
| `docker compose up --no-deps` | Skips starting linked services. |
| `docker compose up --scale service=3` | Sets the number of containers for a service. |
| `docker compose down [OPTIONS]` | Stops and removes containers, networks, and volumes defined by `compose`. |
| `docker compose down -v` | Removes volumes defined by `compose`. |
| `docker compose down --rmi all` | Removes all images used by services. |
| `docker compose ps [OPTIONS] [SERVICE...]` | Lists containers. |
| `docker compose ps -a` | Lists all containers (including stopped ones). |
| `docker compose logs [OPTIONS] [SERVICE...]` | Shows log output from services. |
| `docker compose logs -f` | Follows log output. |
| `docker compose logs --tail=100` | Shows the last 100 lines of logs. |
| `docker compose logs service1 service2` | Shows logs for specific services. |
| `docker compose build [OPTIONS] [SERVICE...]` | Builds or rebuilds services. |
| `docker compose build --no-cache` | Builds images without using cache. |
| `docker compose build --pull` | Always attempts to pull a newer version of the image. |
| `docker compose pull [OPTIONS] [SERVICE...]` | Pulls images for services. |
| `docker compose push [OPTIONS] [SERVICE...]` | Pushes images for services. |
| `docker compose start [OPTIONS] [SERVICE...]` | Starts existing containers for a service. |
| `docker compose stop [OPTIONS] [SERVICE...]` | Stops running containers for a service. |
| `docker compose stop -t 30` | Stops containers with a timeout of 30 seconds. |
| `docker compose restart [OPTIONS] [SERVICE...]` | Restarts containers for a service. |
| `docker compose pause [SERVICE...]` | Pauses running containers for a service. |
| `docker compose unpause [SERVICE...]` | Unpauses paused containers for a service. |
| `docker compose rm [OPTIONS] [SERVICE...]` | Removes stopped service containers. |
| `docker compose rm -f` | Force removes containers. |
| `docker compose rm -sv` | Removes containers and volumes. |
| `docker compose exec [OPTIONS] SERVICE COMMAND [ARGS...]` | Executes a command in a running container. |
| `docker compose exec -it service bash` | Starts an interactive shell in a running container. |
| `docker compose exec -u user:group service command` | Executes a command as a specific user. |
| `docker compose port [OPTIONS] SERVICE PRIVATE_PORT` | Prints the public-facing port for a private port. |
| `docker compose scale SERVICE=NUM` | Sets the number of containers for a service. |
| `docker compose config [OPTIONS]` | Validates and views the Compose file. |
| `docker compose config --services` | Shows the service names. |
| `docker compose config --volumes` | Shows the volume names. |
| `docker compose create [OPTIONS] [SERVICE...]` | Creates containers for a service. |
| `docker compose create --build` | Builds images before creating containers. |
| `docker compose kill [OPTIONS] [SERVICE...]` | Force stops service containers. |
| `docker compose kill -s SIGTERM` | Force stops containers with a specific signal. |
| `docker compose images [OPTIONS] [SERVICE...]` | Lists images used by services. |
| `docker compose top [OPTIONS] [SERVICE...]` | Displays the running processes in services. |
| `docker compose version` | Shows the Docker Compose version. |
| `docker-compose up [OPTIONS] [SERVICE...]` | Legacy command for creating and starting containers (Docker Compose v1). |
| `docker-compose down [OPTIONS]` | Legacy command for stopping and removing containers (Docker Compose v1). |
| `docker-compose ps [OPTIONS] [SERVICE...]` | Legacy command for listing containers (Docker Compose v1). |
| `docker-compose logs [OPTIONS] [SERVICE...]` | Legacy command for showing log output (Docker Compose v1). |

---
## Docker Swarm

| Code | Description |
|------|-------------|
| `docker swarm init [OPTIONS]` | Initializes a new swarm. |
| `docker swarm init --advertise-addr IP:PORT` | Initializes a swarm with a custom advertise address. |
| `docker swarm join [OPTIONS] HOST:PORT` | Joins a swarm as a worker or manager. |
| `docker swarm join --token TOKEN HOST:PORT` | Joins a swarm with a specific token. |
| `docker swarm leave [OPTIONS]` | Leaves the swarm. |
| `docker swarm leave -f` | Force leaves the swarm. |
| `docker node ls [OPTIONS]` | Lists nodes in the swarm. |
| `docker node ls --filter role=manager` | Lists manager nodes in the swarm. |
| `docker node inspect [OPTIONS] [SELF|NODE-ID|NODE-NAME]` | Displays detailed information about one or more nodes. |
| `docker node promote NODE [NODE...]` | Promotes one or more nodes to manager in the swarm. |
| `docker node demote NODE [NODE...]` | Demotes one or more nodes from manager in the swarm. |
| `docker node ps [OPTIONS] [NODE]` | Lists tasks running on one or more nodes. |
| `docker node ps -a` | Lists all tasks (including completed ones). |
| `docker node update [OPTIONS] NODE` | Updates a node. |
| `docker node update --label-add label=value NODE` | Adds a label to a node. |
| `docker node update --label-rm label NODE` | Removes a label from a node. |
| `docker node update --availability drain NODE` | Sets node availability to drain. |
| `docker node update --availability active NODE` | Sets node availability to active. |
| `docker node update --availability pause NODE` | Sets node availability to pause. |
| `docker node rm [OPTIONS] NODE [NODE...]` | Removes one or more nodes from the swarm. |
| `docker node rm -f NODE` | Force removes a node from the swarm. |
| `docker service create [OPTIONS] IMAGE [COMMAND] [ARG...]` | Creates a new service. |
| `docker service create --name myservice IMAGE` | Creates a service with a custom name. |
| `docker service create --replicas=3 IMAGE` | Creates a service with 3 replicas. |
| `docker service create --mode global IMAGE` | Creates a global service. |
| `docker service create --mode replicated --replicas=3 IMAGE` | Creates a replicated service with 3 replicas. |
| `docker service create --network mynetwork IMAGE` | Creates a service connected to a specific network. |
| `docker service create --mount type=bind,source=/host/path,target=/container/path IMAGE` | Creates a service with a bind mount. |
| `docker service create --env VAR=value IMAGE` | Creates a service with environment variables. |
| `docker service create --config source=config,target=/config IMAGE` | Creates a service with a config. |
| `docker service create --secret source=secret,target=/secret IMAGE` | Creates a service with a secret. |
| `docker service create --limit-cpu 2 IMAGE` | Creates a service with CPU limits. |
| `docker service create --limit-memory 512m IMAGE` | Creates a service with memory limits. |
| `docker service ls [OPTIONS]` | Lists services. |
| `docker service ls -a` | Lists all services (including stopped ones). |
| `docker service ls --filter mode=replicated` | Lists replicated services. |
| `docker service inspect [OPTIONS] SERVICE|TASK [SERVICE|TASK...]` | Displays detailed information about one or more services or tasks. |
| `docker service logs [OPTIONS] SERVICE|TASK` | Fetches the logs of a service or task. |
| `docker service logs -f SERVICE` | Follows the logs of a service. |
| `docker service logs --tail 100 SERVICE` | Shows the last 100 lines of logs for a service. |
| `docker service rm [OPTIONS] SERVICE [SERVICE...]` | Removes one or more services. |
| `docker service update [OPTIONS] SERVICE [COMMAND] [ARG...]` | Updates a service. |
| `docker service update --image IMAGE SERVICE` | Updates a service to use a new image. |
| `docker service update --replicas=5 SERVICE` | Updates a service to use 5 replicas. |
| `docker service update --force SERVICE` | Force updates a service. |
| `docker service update --rollback SERVICE` | Rolls back a service to the previous version. |
| `docker service rollback [OPTIONS] SERVICE` | Rolls back a service to the previous version. |
| `docker service scale SERVICE=NUM` | Scales a service to the specified number of replicas. |
| `docker config create [OPTIONS] FILE` | Creates a config from a file. |
| `docker config create --name myconfig FILE` | Creates a config with a custom name. |
| `docker config create --label mylabel=value FILE` | Creates a config with labels. |
| `docker config ls [OPTIONS]` | Lists configs. |
| `docker config inspect [OPTIONS] CONFIG [CONFIG...]` | Displays detailed information about one or more configs. |
| `docker config rm [OPTIONS] CONFIG [CONFIG...]` | Removes one or more configs. |
| `docker secret create [OPTIONS] FILE` | Creates a secret from a file. |
| `docker secret create --name mysecret FILE` | Creates a secret with a custom name. |
| `docker secret create --label mylabel=value FILE` | Creates a secret with labels. |
| `docker secret ls [OPTIONS]` | Lists secrets. |
| `docker secret inspect [OPTIONS] SECRET [SECRET...]` | Displays detailed information about one or more secrets. |
| `docker secret rm [OPTIONS] SECRET [SECRET...]` | Removes one or more secrets. |

---
## Docker Builder (BuildKit)

| Code | Description |
|------|-------------|
| `docker buildx version` | Shows the BuildKit version. |
| `docker buildx ls` | Lists builder instances. |
| `docker buildx create [OPTIONS] [NAME]` | Creates a new builder instance. |
| `docker buildx use [NAME]` | Switches to a builder instance. |
| `docker buildx inspect [OPTIONS] [NAME]` | Inspects a builder instance. |
| `docker buildx rm [OPTIONS] [NAME]` | Removes a builder instance. |
| `docker buildx prune [OPTIONS]` | Removes unused builder instances. |
| `docker buildx build [OPTIONS] PATH` | Builds an image using BuildKit. |
| `docker buildx build -t image:tag --platform linux/amd64,linux/arm64 .` | Builds a multi-platform image. |
| `docker buildx build --push -t image:tag .` | Builds and pushes an image. |
| `docker buildx build --load -t image:tag .` | Builds and loads an image to the local Docker daemon. |
| `docker buildx build --cache-from type=gha .` | Builds an image with cache from GitHub Actions. |
| `docker buildx build --cache-to type=gha,mode=max .` | Builds an image and exports cache to GitHub Actions. |
| `docker buildx build --squash -t image:tag .` | Builds an image and squashes layers into a single layer. |
| `docker buildx build --provenance -t image:tag .` | Builds an image with provenance information. |
| `docker buildx build --sbom -t image:tag .` | Builds an image with SBOM (Software Bill of Materials). |

---
## Docker Context

| Code | Description |
|------|-------------|
| `docker context ls` | Lists contexts. |
| `docker context create [OPTIONS] CONTEXT` | Creates a new context. |
| `docker context create mycontext --docker "host=ssh://user@host"` | Creates a context for a remote Docker host. |
| `docker context inspect [OPTIONS] CONTEXT` | Displays detailed information about a context. |
| `docker context use [OPTIONS] CONTEXT` | Switches to a context. |
| `docker context rm [OPTIONS] CONTEXT [CONTEXT...]` | Removes one or more contexts. |
| `docker context update [OPTIONS] CONTEXT` | Updates a context. |
| `docker context check [OPTIONS] CONTEXT` | Checks if a context is valid. |
| `docker context export [OPTIONS] CONTEXT` | Exports a context to a file. |
| `docker context import [OPTIONS] FILE` | Imports a context from a file. |

---
## Docker Plugin

| Code | Description |
|------|-------------|
| `docker plugin ls [OPTIONS]` | Lists plugins. |
| `docker plugin ls --filter enabled=true` | Lists enabled plugins. |
| `docker plugin inspect [OPTIONS] PLUGIN [PLUGIN...]` | Displays detailed information about one or more plugins. |
| `docker plugin install [OPTIONS] PLUGIN [PLUGIN...]` | Installs a plugin. |
| `docker plugin install --grant-all-permissions PLUGIN` | Installs a plugin with all permissions. |
| `docker plugin install --alias myplugin PLUGIN` | Installs a plugin with an alias. |
| `docker plugin enable [OPTIONS] PLUGIN [PLUGIN...]` | Enables a plugin. |
| `docker plugin disable [OPTIONS] PLUGIN [PLUGIN...]` | Disables a plugin. |
| `docker plugin rm [OPTIONS] PLUGIN [PLUGIN...]` | Removes one or more plugins. |
| `docker plugin rm -f PLUGIN` | Force removes a plugin. |
| `docker plugin push [OPTIONS] PLUGIN [REGISTRY/REPOSITORY[:TAG]]` | Pushes a plugin to a registry. |
| `docker plugin pull [OPTIONS] PLUGIN [REGISTRY/REPOSITORY[:TAG]]` | Pulls a plugin from a registry. |
| `docker plugin create [OPTIONS] PLUGIN` | Creates a plugin from a rootfs bundle. |
| `docker plugin upgrade [OPTIONS] PLUGIN [PLUGIN...]` | Upgrades one or more plugins. |
| `docker plugin set [OPTIONS] PLUGIN KEY=VALUE` | Sets a plugin configuration value. |
| `docker plugin prune [OPTIONS]` | Removes unused plugins. |

---
## Docker Manifest

| Code | Description |
|------|-------------|
| `docker manifest annotate [OPTIONS] MANIFEST LIST` | Annotates a manifest with additional information. |
| `docker manifest create [OPTIONS] MANIFEST LIST [LIST...]` | Creates a manifest list from a list of images. |
| `docker manifest inspect [OPTIONS] MANIFEST [MANIFEST...]` | Displays detailed information about a manifest. |
| `docker manifest push [OPTIONS] MANIFEST [REGISTRY/REPOSITORY[:TAG]]` | Pushes a manifest to a registry. |
| `docker manifest pull [OPTIONS] MANIFEST [REGISTRY/REPOSITORY[:TAG]]` | Pulls a manifest from a registry. |
| `docker manifest rm [OPTIONS] MANIFEST [MANIFEST...]` | Removes one or more manifests. |

---
## Docker Trust

| Code | Description |
|------|-------------|
| `docker trust inspect [OPTIONS] TARGET` | Displays detailed information about the trust status of an image. |
| `docker trust revoke [OPTIONS] TARGET` | Revokes trust for an image. |
| `docker trust sign [OPTIONS] TARGET` | Signs an image. |

---
## Docker Scan

| Code | Description |
|------|-------------|
| `docker scan [OPTIONS] TARGET` | Scans an image for vulnerabilities. |
| `docker scan --file Dockerfile` | Scans a Dockerfile for vulnerabilities. |
| `docker scan --severity high` | Scans for vulnerabilities with high severity. |
| `docker scan --verbose` | Scans with verbose output. |

---
## Docker System Commands

| Code | Description |
|------|-------------|
| `docker --help` | Shows Docker help. |
| `docker --version` | Shows Docker version. |
| `docker login [OPTIONS] [SERVER]` | Logs in to a Docker registry. |
| `docker login -u username -p password` | Logs in to a Docker registry with username and password. |
| `docker login --password-stdin` | Logs in to a Docker registry with password from stdin. |
| `docker logout [SERVER]` | Logs out from a Docker registry. |
| `docker search [OPTIONS] TERM` | Searches Docker Hub for images. |
| `docker search --filter is-official=true TERM` | Searches for official images. |
| `docker search --limit 10 TERM` | Limits search results to 10. |
| `docker system df [OPTIONS]` | Shows Docker disk usage. |
| `docker system df -v` | Shows Docker disk usage with verbose output. |
| `docker system events [OPTIONS]` | Gets real-time events from the Docker server. |
| `docker system info [OPTIONS]` | Displays system-wide information. |
| `docker system prune [OPTIONS]` | Removes unused data. |
| `docker system prune -a` | Removes all unused containers, networks, images, and volumes. |
| `docker system prune --volumes` | Removes unused volumes. |

---
## Bash Scripting with Docker

| Code | Description |
|------|-------------|
| `docker run -d --name myapp myimage && docker logs -f myapp` | Runs a container in detached mode and follows its logs. |
| `docker ps -q | xargs docker rm -f` | Removes all running containers. |
| `docker ps -aq | xargs docker rm -f` | Removes all containers (running and stopped). |
| `docker images -q | xargs docker rmi -f` | Removes all images. |
| `docker volume ls -q | xargs docker volume rm -f` | Removes all volumes. |
| `docker network ls -q | xargs docker network rm -f` | Removes all networks. |
| `docker system prune -a -f --volumes` | Removes all unused Docker objects (containers, images, volumes, networks). |
| `for container in $(docker ps -aq); do docker stop $container; done` | Stops all running containers. |
| `for image in $(docker images -q); do docker rmi -f $image; done` | Removes all images. |
| `docker build -t myimage . && docker run -d --name myapp myimage` | Builds an image and runs a container from it. |
| `docker-compose -f docker-compose.yml up -d` | Starts services defined in a Compose file in detached mode. |
| `docker-compose -f docker-compose.yml down -v` | Stops and removes containers and volumes defined in a Compose file. |
| `docker exec -it mycontainer bash -c "command1 && command2"` | Executes multiple commands in a running container. |
| `docker run --rm -v $(pwd):/app -w /app myimage command` | Runs a container, mounts the current directory, and removes it after exit. |
| `docker run --rm -v /host/path:/container/path myimage command` | Runs a container with a volume mount and removes it after exit. |
| `docker run -p 8080:80 myimage` | Runs a container with port mapping. |
| `docker run -e VAR1=value1 -e VAR2=value2 myimage` | Runs a container with environment variables. |
| `docker run --env-file .env myimage` | Runs a container with environment variables from a file. |
| `docker run --network host myimage` | Runs a container with host network mode. |
| `docker run --network mynetwork myimage` | Runs a container connected to a custom network. |
| `docker run --dns 8.8.8.8 myimage` | Runs a container with a custom DNS server. |
| `docker run --dns-search example.com myimage` | Runs a container with a custom DNS search domain. |
| `docker run --hostname myhost myimage` | Runs a container with a custom hostname. |
| `docker run --mac-address MAC myimage` | Runs a container with a custom MAC address. |
| `docker run --cpus=2 myimage` | Runs a container with CPU limits. |
| `docker run --memory=512m myimage` | Runs a container with memory limits. |
| `docker run --restart=always myimage` | Runs a container with a restart policy. |
| `docker run --read-only myimage` | Runs a container with a read-only filesystem. |