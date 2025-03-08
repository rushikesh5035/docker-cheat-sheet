# Docker Commands 🐳

---

## 1. Commands for Images 🖼️

| Command                           | Example                                         | Description                                        |
| --------------------------------- | ----------------------------------------------- | -------------------------------------------------- |
| `docker images`                   | `docker images`                                 | List all Docker images on the host machine.        |
| `docker pull <image>`             | `docker pull ubuntu`                            | 🔽 Download an image from the Docker Hub registry. |
| `docker rmi <image>`              | `docker rmi ubuntu`                             | ❌ Remove a Docker image.                          |
| `docker build -t <image_name> .`  | `docker build -t my_app .`                      | 🏠 Build a Docker image from a `Dockerfile`.       |
| `docker tag <source> <target>`    | `docker tag ubuntu:latest myrepo/ubuntu:custom` | 🌂 Create a new tag for an image.                  |
| `docker inspect <image>`          | `docker inspect ubuntu`                         | 🔍 View detailed information about an image.       |
| `docker history <image>`          | `docker history ubuntu:latest`                  | ⏲ Show the history of an image’s layers.           |
| `docker image prune`              | `docker image prune`                            | 🪩 Remove dangling (unused) images.                 |
| `docker save -o <file.tar> <img>` | `docker save -o ubuntu.tar ubuntu:latest`       | 💾 Save a Docker image as a tar file.              |
| `docker load -i <file.tar>`       | `docker load -i ubuntu.tar`                     | 📂 Load a Docker image from a tar file.            |

---

## 2. Commands for Containers 📦

| Command                           | Example                                           | Description                                               |
| --------------------------------- | ------------------------------------------------- | --------------------------------------------------------- |
| `docker ps`                       | `docker ps`                                       | 🟢 List all running containers.                           |
| `docker ps -a`                    | `docker ps -a`                                    | 📜 List all containers (running and stopped).             |
| `docker run <image>`              | `docker run ubuntu`                               | ▶️ Run a container from a specific image.                 |
| `docker run -it <image>`          | `docker run -it ubuntu bash`                      | 🖥️ Run a container interactively with a terminal session. |
| `docker start <container>`        | `docker start my_container`                       | 🔄 Start a stopped container.                             |
| `docker stop <container>`         | `docker stop my_container`                        | 🛑 Stop a running container.                              |
| `docker restart <container>`      | `docker restart my_container`                     | 🔁 Restart a running container.                           |
| `docker rm <container>`           | `docker rm my_container`                          | 🗑️ Remove a stopped container.                            |
| `docker exec <container> <cmd>`   | `docker exec my_container ls`                     | 🏃 Run a command inside a running container.              |
| `docker exec -it <container>`     | `docker exec -it my_container bash`               | 🖥️ Access the shell of a running container interactively. |
| `docker logs <container>`         | `docker logs my_container`                        | 📜 View logs of a container.                              |
| `docker inspect <container>`      | `docker inspect my_container`                     | 🔍 View detailed information about a container.           |
| `docker diff <container>`         | `docker diff my_container`                        | 🔧 Inspect changes made to a container's filesystem.      |
| `docker cp <container>:<path>`    | `docker cp my_container:/app/file.txt ./file.txt` | 📤 Copy files from a container to the host system.        |
| `docker commit <container> <img>` | `docker commit my_container my_custom_image`      | 🖼️ Create a new image from an existing container.         |
| `docker stats`                    | `docker stats`                                    | 📊 Display resource usage of running containers.          |

---

## 3. Commands for Networks 🌐

| Command                            | Example                                             | Description                               |
| ---------------------------------- | --------------------------------------------------- | ----------------------------------------- |
| `docker network ls`                | `docker network ls`                                 | 📜 List all Docker networks.              |
| `docker network inspect <name>`    | `docker network inspect bridge`                     | 🔍 Inspect a Docker network.              |
| `docker network create <name>`     | `docker network create my_network`                  | 🛠️ Create a new Docker network.           |
| `docker network connect <name>`    | `docker network connect my_network my_container`    | 🔗 Connect a container to a network.      |
| `docker network disconnect <name>` | `docker network disconnect my_network my_container` | ❌ Disconnect a container from a network. |
| `docker network prune`             | `docker network prune`                              | 🪩 Remove unused networks.                 |

---

## 4. Commands for Volumes 📂

| Command                        | Example                           | Description                    |
| ------------------------------ | --------------------------------- | ------------------------------ |
| `docker volume ls`             | `docker volume ls`                | 📜 List all Docker volumes.    |
| `docker volume create <name>`  | `docker volume create my_volume`  | 🛠️ Create a new Docker volume. |
| `docker volume inspect <name>` | `docker volume inspect my_volume` | 🔍 Inspect a Docker volume.    |
| `docker volume rm <name>`      | `docker volume rm my_volume`      | 🗑️ Remove a Docker volume.     |
| `docker volume prune`          | `docker volume prune`             | 🪩 Remove unused volumes.       |

---

## 5. Commands for Docker Compose 🛠️

| Command                     | Example                        | Description                                                             |
| --------------------------- | ------------------------------ | ----------------------------------------------------------------------- |
| `docker-compose up`         | `docker-compose up`            | 🚀 Start containers using a `docker-compose.yml` file.                  |
| `docker-compose down`       | `docker-compose down`          | 🛑 Stop and remove containers defined in the `docker-compose.yml` file. |
| `docker-compose logs`       | `docker-compose logs`          | 📜 View logs for containers managed by Docker Compose.                  |
| `docker-compose ps`         | `docker-compose ps`            | 📜 List running containers managed by Docker Compose.                   |
| `docker-compose exec <cmd>` | `docker-compose exec app bash` | 🖥️ Execute a command inside a service container.                        |
| `docker-compose restart`    | `docker-compose restart`       | 🔁 Restart all services defined in `docker-compose.yml`.                |

---

## 6. Commands for Troubleshooting 🛠️

| Command                             | Example                             | Description                                                          |
| ----------------------------------- | ----------------------------------- | -------------------------------------------------------------------- |
| `docker logs <container>`           | `docker logs my_container`          | 📜 View logs of a container to troubleshoot errors.                  |
| `docker logs -f <container>`        | `docker logs -f my_container`       | 🔄 Follow (stream) the container logs in real time.                  |
| `docker exec -it <container> bash`  | `docker exec -it my_container bash` | 🖥️ Access the container's shell to debug issues inside it.           |
| `docker inspect <container_or_img>` | `docker inspect my_container`       | 🔍 Get detailed JSON information about a container or image.         |
| `docker top <container>`            | `docker top my_container`           | 📊 Display the processes running inside a container.                 |
| `docker stats`                      | `docker stats`                      | 📈 Monitor resource usage (CPU, memory, etc.) of running containers. |
| `docker diff <container>`           | `docker diff my_container`          | 🔧 Inspect changes made to a container's filesystem.                 |
| `docker events`                     | `docker events`                     | 📡 Display real-time events from the Docker daemon.                  |
| `docker system df`                  | `docker system df`                  | 🐂 Show disk space usage by Docker resources.                        |

---

## 7. Commands for Docker Hub Operations 🌐

| Command                            | Example                                           | Description                                         |
| ---------------------------------- | ------------------------------------------------- | --------------------------------------------------- |
| `docker login`                     | `docker login`                                    | 🔑 Log in to your Docker Hub account.               |
| `docker logout`                    | `docker logout`                                   | ❌ Log out of your Docker Hub account.              |
| `docker pull <image>`              | `docker pull nginx`                               | 🔽 Pull an image from Docker Hub.                   |
| `docker push <image>`              | `docker push myrepo/myimage:latest`               | 📤 Push an image to your Docker Hub repository.     |
| `docker tag <source> <repo/image>` | `docker tag myimage:latest myrepo/myimage:latest` | 🌂 Tag a local image for pushing to Docker Hub.     |
| `docker search <term>`             | `docker search nginx`                             | 🔍 Search for images on Docker Hub using a keyword. |

---

## 8. Other Useful Docker Commands 🛠️

| Command                  | Example                   | Description                                          |
| ------------------------ | ------------------------- | ---------------------------------------------------- |
| `docker system prune`    | `docker system prune`     | 🪩 Remove unused images, containers, and volumes.     |
| `docker events`          | `docker events`           | 📡 Display real-time events from the Docker daemon.  |
| `docker top <container>` | `docker top my_container` | 📊 Display the processes running inside a container. |
