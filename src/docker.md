# Docker Cheat Sheet

A quick reference for the most common Docker commands and concepts.

---

## 🐳 Basic Commands

- `docker --version`  
Check Docker version.

- `docker info`  
Display system-wide information.

- `docker help`  
List all commands.

---

## 🏗️ Working with Images

- `docker pull <image>`  
Download an image from Docker Hub.

- `docker images`  
List all downloaded images.

- `docker rmi <image>`  
Remove an image.

- `docker build -t <name>:<tag> .`  
Build an image from a Dockerfile.

- `docker tag <image> <repository>:<tag>`  
Tag an image.

---

## 🚢 Working with Containers

- `docker run <image>`  
Run a container from an image.

- `docker run -it <image>`  
Run interactively with a terminal.

- `docker run -d <image>`  
Run in detached mode (background).

- `docker run -p <host_port>:<container_port> <image>`  
Map ports.

- `docker run --name <name> <image>`  
Run with a specific container name.

- `docker ps`  
List running containers.

- `docker ps -a`  
List all containers (including stopped).

- `docker stop <container>`  
Stop a running container.

- `docker start <container>`  
Start a stopped container.

- `docker restart <container>`  
Restart a container.

- `docker rm <container>`  
Remove a stopped container.

- `docker exec -it <container> <command>`  
Execute a command inside a running container.

- `docker logs <container>`  
View container logs.

---

## 🗄️ Volumes

- `docker volume create <name>`  
Create a volume.

- `docker volume ls`  
List volumes.

- `docker volume inspect <name>`  
Inspect volume details.

- `docker run -v <volume>:/path/in/container <image>`  
Mount a volume.

---

## 🌐 Networks

- `docker network ls`  
List networks.

- `docker network create <name>`  
Create a network.

- `docker network inspect <name>`  
Inspect a network.

- `docker run --network=<name> <image>`  
Connect container to a specific network.

---

## 📦 Docker Compose

- `docker-compose up`  
Start services defined in `docker-compose.yml`.

- `docker-compose up -d`  
Start services in detached mode.

- `docker-compose down`  
Stop and remove services.

- `docker-compose ps`  
List services.

- `docker-compose logs`  
View service logs.

---

## 🧹 Clean up

- `docker system prune`  
Remove unused data.

- `docker image prune`  
Remove unused images.

- `docker volume prune`  
Remove unused volumes.

- `docker container prune`  
Remove stopped containers.

---

## 📝 Useful Tips

- Use `.dockerignore` to avoid copying unnecessary files.
- Always specify versions/tags for images to avoid unexpected updates.
- Use multi-stage builds for smaller and more secure images.
- Prefer volumes over bind mounts for persistent data.

---

## 📚 Resources

- [Docker Docs](https://docs.docker.com/)
- [Docker Hub](https://hub.docker.com/)

---


[Voltar para HOME](https://github.com/pvstelles/cheat-sheet/blob/main/README.md)

Happy Dockering! 🚀
