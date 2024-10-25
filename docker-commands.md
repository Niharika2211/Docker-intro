To create a Markdown file (.md) for these Docker commands for a GitHub repository, let's format it so the commands are easy to read and copy. This file will be called `Docker_Commands.md`.

Here's the structured Markdown content:

```markdown
# Docker Cheat Sheet

## Docker Overview

- **Virtualization**: Divides a large physical server into multiple logical servers, often using a hypervisor.
- **Microservices & Containers**: Containers facilitate microservices, allowing efficient resource utilization with minimal footprint and faster boot times.
- **Portability**: Docker images are similar to AMIs, designed for easy movement and reuse across environments.

## Docker Image Structure

- A Docker image consists of:
  - A **bare minimum OS** (without unnecessary packages)
  - **App runtime** (e.g., Java, Node.js, Python)
  - **System packages and dependencies**
  - **Application code**

## Docker Installation

Install Docker according to your OS (e.g., RHEL, Ubuntu). After installation, Docker creates a group, and only users in this group can run Docker commands.

## Common Docker Commands

### Basic Commands

```bash
docker images                       # List Docker images
docker pull <image-name>            # Pull image from DockerHub
docker create <image>:<tag>         # Create a container from an image
docker ps                           # List running containers
docker ps -a                        # List all containers with their statuses
docker start <CONTAINER ID>         # Start a stopped container
docker rm <CONTAINER ID>            # Remove a container
docker rm -f <CONTAINER ID>         # Force remove a running container
docker rmi <image ID>               # Remove an image
docker tag <image ID> <new-tag>     # Tag an image with a new version
```

### Running Containers

```bash
docker run <image-name>             # Pull, create, and run a container in one command
docker run -d <image-name>          # Run container in detached mode (background)
docker run -d -p <host-port>:<container-port> <image-name>   # Run container with port forwarding
```

### Bulk Removal of Images and Containers

```bash
docker rmi $(docker images -a -q)   # Remove all images
docker rm -f $(docker ps -a -q)     # Remove all containers
```

### Notes on Efficiency

- **Minimal Size**: Docker images are lightweight, with a reduced footprint, taking up less disk space and requiring fewer CPU and memory resources compared to virtual machines.
- **Portability**: Docker images, like AMIs, are easy to move and deploy consistently across environments.

---

### Accessing Docker Containers from the Internet

To allow internet access to a Docker container, forward the desired host port to the container port using the following command:

```bash
docker run -d -p <host-port>:<container-port> <container-name>
```

---
