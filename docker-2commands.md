
```markdown
# 🐳 Docker Cheat Sheet

## 📦 Container Metadata and Information
- **Inspect a running container** to get detailed information:

  ```bash
  docker inspect <container_id>
  ```

- **Inspect an image** to get metadata:
  ```bash
  docker inspect <image_id>
  ```

## 📋 Viewing Container Logs
- **Show logs** of a container:
  ```bash
  docker logs <container_id>
  ```
- **Stream logs** in real-time (`-f` is for "follow"):
  ```bash
  docker logs -f <container_id>
  ```

## 🔄 Interacting with Containers
- **Access the terminal** of a running container:
  ```bash
  docker exec -it <container_id> bash
  ```
  > If the container uses a different shell (like `sh`), use:
  ```bash
  docker exec -it <container_id> sh
  ```

## 🚀 Useful Docker Commands for Management
- **Stop a running container**:
  ```bash
  docker stop <container_id>
  ```

### 🔧 System Cleanup
- **Remove all stopped containers, unused networks, and dangling images**:
  ```bash
  docker system prune -a
  ```

### 📂 Volumes and Networks
- **List Docker volumes**:
  ```bash
  docker volume ls
  ```

---

### 📄 Notes
- Replace `<container_id>` or `<image_id>` with the respective IDs.
- Use `docker ps` to get the container IDs of running containers.
- Use `docker images` to get the image IDs.

Happy Dockerizing! 🐋🚀
