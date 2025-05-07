## 📦 Docker Image Commands
---

| 🛠️ Command    | 📄 Description                              | 🧪 Example                                | 🔤 Icon |
| -------------- | ------------------------------------------- | ----------------------------------------- | ------- |
| docker build   | Build an image from a Dockerfile            | ```bash\ndocker build -t myapp .\n```     | 🏗️     |
| docker images  | List local images                           | ```bash\ndocker images\n```               | 📋      |
| docker rmi     | Remove one or more images                   | ```bash\ndocker rmi myapp:latest\n```     | ❌       |
| docker tag     | Tag an image for a repository               | ```bash\ndocker tag myapp user/myapp:1.0\n``` | 🏷️     |
| docker pull    | Pull an image from Docker Hub               | ```bash\ndocker pull nginx\n```           | ⬇️      |
| docker push    | Push an image to a registry                 | ```bash\ndocker push user/myapp\n```      | ⬆️      |
| docker save    | Save image(s) to a tar archive              | ```bash\ndocker save -o app.tar myapp:latest\n``` | 💾      |
| docker load    | Load image from a tar archive               | ```bash\ndocker load -i app.tar\n```      | 📂      |
| docker inspect | Detailed info about image/container/network | ```bash\ndocker inspect nginx\n```        | 🔍      |

## 📁 Docker Volume Commands

---

| 🛠️ Command           | 📄 Description            | 🧪 Example                         | 🔤 Icon |
| --------------------- | ------------------------- | ---------------------------------- | ------- |
| docker volume create  | Create a volume           | `docker volume create myvol`       | ➕       |
| docker volume ls      | List all volumes          | `docker volume ls`                 | 📋      |
| docker volume inspect | Show volume details       | `docker volume inspect myvol`      | 🔍      |
| docker volume rm      | Remove a volume           | `docker volume rm myvol`           | ❌       |
| docker run -v         | Mount volume to container | `docker run -v myvol:/data alpine` | 📦      |

## 🌐 Docker Network Commands

--

| 🛠️ Command            | 📄 Description                 | 🧪 Example                         | 🔤 Icon |
| ---------------------- | ------------------------------ | ---------------------------------- | ------- |
| docker network create  | Create a new network           | `docker network create mynet`      | 🌐      |
| docker network ls      | List all networks              | `docker network ls`                | 📋      |
| docker network inspect | View detailed network config   | `docker network inspect mynet`     | 🔍      |
| docker network rm      | Remove a network               | `docker network rm mynet`          | ❌       |
| docker run --network   | Connect container to a network | `docker run --network=mynet nginx` | 🔌      |

## 🧬 Docker Compose Commands

---

| 🛠️ Command          | 📄 Description                              | 🧪 Example                     | 🔤 Icon |
| -------------------- | ------------------------------------------- | ------------------------------ | ------- |
| docker-compose up    | Start services                              | `docker-compose up`            | ▶️      |
| docker-compose down  | Stop and remove containers/networks/volumes | `docker-compose down`          | ⏹️      |
| docker-compose build | Build or rebuild services                   | `docker-compose build`         | 🏗️     |
| docker-compose ps    | List containers                             | `docker-compose ps`            | 📋      |
| docker-compose logs  | View logs                                   | `docker-compose logs -f`       | 📜      |
| docker-compose exec  | Run command in a running service            | `docker-compose exec web bash` | 💬      |

## 🧹 Docker System Cleanup

---

| 🛠️ Command            | 📄 Description            | 🧪 Example               | 🔤 Icon |
| ---------------------- | ------------------------- | ------------------------ | ------- |
| docker system prune    | Remove unused data        | `docker system prune -a` | 🧹      |
| docker image prune     | Remove unused images      | `docker image prune`     | 🖼️     |
| docker volume prune    | Remove unused volumes     | `docker volume prune`    | 📦      |
| docker container prune | Remove stopped containers | `docker container prune` | 🚮      |
| docker network prune   | Remove unused networks    | `docker network prune`   | 🌐      |

## 🛠️ Docker Troubleshooting Commands

---

| 🛠️ Command     | 📄 Description                          | 🧪 Example                   | 🔤 Icon |
| --------------- | --------------------------------------- | ---------------------------- | ------- |
| docker logs     | View logs from a container              | `docker logs myapp`          | 📜      |
| docker ps -a    | List all containers                     | `docker ps -a`               | 📋      |
| docker top      | Show running processes in a container   | `docker top myapp`           | 🧠      |
| docker events   | Real-time events from the Docker daemon | `docker events`              | 📡      |
| docker stats    | Live resource usage stats               | `docker stats`               | 📈      |
| docker exec -it | Run command inside running container    | `docker exec -it myapp bash` | 🔧      |
| docker inspect  | Detailed JSON output about resources    | `docker inspect myapp`       | 🔍      |


## 🛠️ Dockerfile Commands – Complete List with Explanations & Icons

---

| 🔤 Command    | 🧠 Description                                                                                | 🧪 Example                                                                   | 🪄 Icon |
|--------------|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------|
| FROM         | Sets the base image for the Docker image. Must be the first command.                          | `FROM node:18-alpine`                                                        | 📦      |
| LABEL        | Adds metadata to the image (e.g. author, description).                                        | `LABEL maintainer="you@example.com"`                                         | 🏷️     |
| ENV          | Sets environment variables used in the image.                                                 | `ENV NODE_ENV=production`                                                    | 🌿      |
| ARG          | Defines build-time variables (not available at runtime unless passed).                        | `ARG VERSION=1.0`                                                            | 🧩      |
| RUN          | Executes shell commands during image build (creates image layers).                            | `RUN apt-get update && apt-get install -y curl`                              | ⚙️      |
| COPY         | Copies files/directories from host (build context) into the image.                            | `COPY ./app /usr/src/app`                                                    | 📁      |
| ADD          | Like COPY, but supports remote URLs and auto-unpacks tar files.                               | `ADD app.tar.gz /usr/src/app/`                                               | ➕      |
| WORKDIR      | Sets the working directory for subsequent instructions.                                       | `WORKDIR /usr/src/app`                                                       | 📂      |
| EXPOSE       | Documents the port the container listens on (doesn't publish it).                             | `EXPOSE 3000`                                                                | 🌐      |
| CMD          | Sets default command to run on container start (can be overridden).                           | `CMD ["node", "server.js"]`                                                  | ▶️      |
| ENTRYPOINT   | Sets a command to always run and is less easily overridden than CMD.                          | `ENTRYPOINT ["docker-entrypoint.sh"]`                                        | 🚪      |
| VOLUME       | Defines a mount point with a specified path for persistent/shared data.                       | `VOLUME /data`                                                               | 💾      |
| USER         | Sets the username or UID to run container processes.                                          | `USER node`                                                                  | 👤      |
| SHELL        | Changes the default shell used for RUN, CMD, ENTRYPOINT.                                      | `SHELL ["powershell", "-command"]`                                           | 🐚      |
| HEALTHCHECK  | Defines a command to test container health.                                                   | `HEALTHCHECK CMD curl --fail http://localhost:3000 || exit 1`                | ❤️      |
| ONBUILD      | Trigger instruction for when the image is used as a base in another build.                    | `ONBUILD COPY . /app`                                                        | 🧨      |
| STOPSIGNAL   | Sets the system call signal to stop the container.                                            | `STOPSIGNAL SIGTERM`                                                         | 🛑      |


## 