### Docker Basics

#### 1. **Check Docker Version**
Check the installed Docker version:
```bash
docker --version
```

#### 2. **List Docker Containers**
List all running containers:
```bash
docker ps
```

List all containers, including stopped ones:
```bash
docker ps -a
```

#### 3. **Start a Container**
Start a container by its name or ID:
```bash
docker start <container_name_or_id>
```

#### 4. **Stop a Container**
Stop a running container:
```bash
docker stop <container_name_or_id>
```

#### 5. **Restart a Container**
Restart a container (stop and start again):
```bash
docker restart <container_name_or_id>
```

#### 6. **Remove a Container**
Remove a stopped container:
```bash
docker rm <container_name_or_id>
```

To force-remove a running container:
```bash
docker rm -f <container_name_or_id>
```

#### 7. **Inspect a Container**
View detailed information about a container:
```bash
docker inspect <container_name_or_id>
```

#### 8. **View Container Logs**
View logs of a container:
```bash
docker logs <container_name_or_id>
```

You can also use `-f` to follow the logs in real-time:
```bash
docker logs -f <container_name_or_id>
```

---

### Docker Images

#### 9. **List Docker Images**
List all Docker images on your system:
```bash
docker images
```

#### 10. **Pull an Image**
Pull a Docker image from Docker Hub (e.g., for PostgreSQL):
```bash
docker pull <image_name>
```
Example:
```bash
docker pull postgres
```

#### 11. **Build an Image**
Build an image from a `Dockerfile` in the current directory:
```bash
docker build -t <image_name>:<tag> .
```
Example:
```bash
docker build -t myapp:latest .
```

#### 12. **Remove an Image**
Remove a Docker image:
```bash
docker rmi <image_name_or_id>
```

You can also force-remove an image if it’s being used by a container:
```bash
docker rmi -f <image_name_or_id>
```

#### 13. **Tag an Image**
Tag an image with a different name or version:
```bash
docker tag <image_name>:<old_tag> <image_name>:<new_tag>
```
Example:
```bash
docker tag myapp:latest myapp:v1
```

#### 14. **Push an Image**
Push a Docker image to a registry (like Docker Hub):
```bash
docker push <image_name>:<tag>
```
Example:
```bash
docker push myapp:latest
```

---

### Docker Volumes (Data Persistence)

#### 15. **List Volumes**
List all Docker volumes:
```bash
docker volume ls
```

#### 16. **Create a Volume**
Create a new volume:
```bash
docker volume create <volume_name>
```

#### 17. **Remove a Volume**
Remove a volume:
```bash
docker volume rm <volume_name>
```

#### 18. **Inspect a Volume**
Get details about a specific volume:
```bash
docker volume inspect <volume_name>
```

---

### Docker Networks (Container Communication)

#### 19. **List Networks**
List all Docker networks:
```bash
docker network ls
```

#### 20. **Create a Network**
Create a new Docker network:
```bash
docker network create <network_name>
```

#### 21. **Remove a Network**
Remove a Docker network:
```bash
docker network rm <network_name>
```

#### 22. **Connect a Container to a Network**
Connect a running container to a network:
```bash
docker network connect <network_name> <container_name_or_id>
```

#### 23. **Disconnect a Container from a Network**
Disconnect a running container from a network:
```bash
docker network disconnect <network_name> <container_name_or_id>
```

---

### Docker Compose (For Multi-Container Applications)

#### 24. **Run Docker Compose**
If you have a `docker-compose.yml` file, you can use this command to start your services:
```bash
docker-compose up
```

Run in detached mode (in the background):
```bash
docker-compose up -d
```

#### 25. **Stop Docker Compose**
Stop all containers in the current Docker Compose project:
```bash
docker-compose down
```

#### 26. **Build Docker Compose Services**
Rebuild the services in your Docker Compose project:
```bash
docker-compose build
```

---

### Docker System Cleanup

#### 27. **Remove Unused Docker Objects**
To clean up unused containers, images, volumes, and networks:
```bash
docker system prune
```

You can use `-a` to remove **all unused images** (not just dangling ones):
```bash
docker system prune -a
```

#### 28. **Remove Stopped Containers**
Remove all stopped containers:
```bash
docker container prune
```

#### 29. **Remove Unused Images**
Remove all unused Docker images:
```bash
docker image prune
```

---

### Useful Docker Shortcuts

#### 30. **Docker Help**
To get help for a Docker command:
```bash
docker help
```

Or for a specific command:
```bash
docker <command> --help
```

---

### Example Workflow
1. **Start a container:**
   ```bash
   docker start my_container
   ```

2. **View logs of a running container:**
   ```bash
   docker logs -f my_container
   ```

3. **Stop a container:**
   ```bash
   docker stop my_container
   ```

4. **Remove a container:**
   ```bash
   docker rm my_container
   ```

5. **Remove an image:**
   ```bash
   docker rmi my_image
   ```
