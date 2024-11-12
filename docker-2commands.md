
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

### 🛠️ Container Management
- **List all containers** (running and stopped):
  ```bash
  docker ps -a
  ```
- **Stop a running container**:
  ```bash
  docker stop <container_id>
  ```
- **Remove a stopped container**:
  ```bash
  docker rm <container_id>
  ```

### 🗑️ Image Management
- **List all Docker images**:
  ```bash
  docker images
  ```
- **Remove an image**:
  ```bash
  docker rmi <image_id>
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
- **List Docker networks**:
  ```bash
  docker network ls
  ```

---

### 📄 Notes
- Replace `<container_id>` or `<image_id>` with the respective IDs.
- Use `docker ps` to get the container IDs of running containers.
- Use `docker images` to get the image IDs.

---

📝 **Pro Tip**: You can copy and paste these commands directly into your terminal or use this Markdown file in your Git repository for quick reference.

---

Happy Dockerizing! 🐋🚀
```

Feel free to copy this into your Git repo or adjust it as needed. Let me know if there's anything else you’d like to add!
