# Docker Cheat Sheet

This cheat sheet provides a quick reference for basic Docker commands.

## Image Management

| Command | Description |
| :--- | :--- |
| `docker build -t {image_name}:{tag} .` | Build an image from a Dockerfile in the current directory. |
| `docker images` or `docker image ls` | List all local images. |
| `docker rmi {image_id_or_name}` | Remove a local image. |
| `docker pull {image_name}:{tag}` | Pull an image from a registry (e.g., Docker Hub). |
| `docker tag {source_image} {target_image}` | Create a tag for a source image. |
| `docker history {image_name}` | Show the history of an image. |
| `docker inspect {image_name_or_id}` | Display detailed information on one or more images. |

## Container Lifecycle

| Command | Description |
| :--- | :--- |
| `docker run {image_name}` | Create and start a new container from an image. |
| `docker run -d -p {host_port}:{container_port} --name {container_name} {image_name}` | Run a container in detached mode with port mapping. |
| `docker ps` | List all running containers. |
| `docker ps -a` | List all containers (running and stopped). |
| `docker stop {container_id_or_name}` | Stop a running container. |
| `docker start {container_id_or_name}` | Start a stopped container. |
| `docker restart {container_id_or_name}` | Restart a container. |
| `docker rm {container_id_or_name}` | Remove a stopped container. |
| `docker rm -f {container_id_or_name}` | Force-remove a running container. |

## Interacting with Containers

| Command | Description |
| :--- | :--- |
| `docker exec -it {container_id_or_name} /bin/bash` | Get an interactive shell inside a running container. |
| `docker logs {container_id_or_name}` | Fetch the logs of a container. |
| `docker logs -f {container_id_or_name}` | Follow the log output of a container. |
| `docker cp {host_path} {container_id}:{container_path}` | Copy files from the host to a container. |
| `docker cp {container_id}:{container_path} {host_path}` | Copy files from a container to the host. |

## Docker Hub / Registry

| Command | Description |
| :--- | :--- |
| `docker login` | Log in to a Docker registry. |
| `docker logout` | Log out from a Docker registry. |
| `docker push {image_name}:{tag}` | Push an image to a registry. |
| `docker search {term}` | Search Docker Hub for images. |

## Docker Compose

| Command | Description |
| :--- | :--- |
| `docker compose up` | Create and start containers defined in `docker-compose.yml`. |
| `docker compose up -d` | Create and start containers in detached mode. |
| `docker compose down` | Stop and remove containers, networks, and volumes. |
| `docker compose ps` | List containers for the current project. |
| `docker compose logs` | View output from services. |
| `docker compose build` | Build or rebuild services. |
| `docker compose exec {service_name} {command}` | Execute a command in a running service. |

## System & Cleanup

| Command | Description |
| :--- | :--- |
| `docker system prune` | Remove all unused containers, networks, and dangling images. |
| `docker system prune -a --volumes` | Remove all unused images, containers, networks, and volumes. |
| `docker info` | Display system-wide information. |
| `docker version` | Show the Docker version information. |
