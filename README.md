## 📦 Docker Image Commands

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

---

## 📁 Docker Volume Commands

| 🛠️ Command           | 📄 Description            | 🧪 Example                         | 🔤 Icon |
| --------------------- | ------------------------- | ---------------------------------- | ------- |
| docker volume create  | Create a volume           | `docker volume create myvol`       | ➕       |
| docker volume ls      | List all volumes          | `docker volume ls`                 | 📋      |
| docker volume inspect | Show volume details       | `docker volume inspect myvol`      | 🔍      |
| docker volume rm      | Remove a volume           | `docker volume rm myvol`           | ❌       |
| docker run -v         | Mount volume to container | `docker run -v myvol:/data alpine` | 📦      |

---

## 🌐 Docker Network Commands

| 🛠️ Command            | 📄 Description                 | 🧪 Example                         | 🔤 Icon |
| ---------------------- | ------------------------------ | ---------------------------------- | ------- |
| docker network create  | Create a new network           | `docker network create mynet`      | 🌐      |
| docker network ls      | List all networks              | `docker network ls`                | 📋      |
| docker network inspect | View detailed network config   | `docker network inspect mynet`     | 🔍      |
| docker network rm      | Remove a network               | `docker network rm mynet`          | ❌       |
| docker run --network   | Connect container to a network | `docker run --network=mynet nginx` | 🔌      |

---


## 🧬 Docker Compose Commands

| 🛠️ Command          | 📄 Description                              | 🧪 Example                     | 🔤 Icon |
| -------------------- | ------------------------------------------- | ------------------------------ | ------- |
| docker-compose up    | Start services                              | `docker-compose up`            | ▶️      |
| docker-compose down  | Stop and remove containers/networks/volumes | `docker-compose down`          | ⏹️      |
| docker-compose build | Build or rebuild services                   | `docker-compose build`         | 🏗️     |
| docker-compose ps    | List containers                             | `docker-compose ps`            | 📋      |
| docker-compose logs  | View logs                                   | `docker-compose logs -f`       | 📜      |
| docker-compose exec  | Run command in a running service            | `docker-compose exec web bash` | 💬      |

---

## 🧹 Docker System Cleanup

| 🛠️ Command            | 📄 Description            | 🧪 Example               | 🔤 Icon |
| ---------------------- | ------------------------- | ------------------------ | ------- |
| docker system prune    | Remove unused data        | `docker system prune -a` | 🧹      |
| docker image prune     | Remove unused images      | `docker image prune`     | 🖼️     |
| docker volume prune    | Remove unused volumes     | `docker volume prune`    | 📦      |
| docker container prune | Remove stopped containers | `docker container prune` | 🚮      |
| docker network prune   | Remove unused networks    | `docker network prune`   | 🌐      |

---

## 🛠️ Docker Troubleshooting Commands

| 🛠️ Command     | 📄 Description                          | 🧪 Example                   | 🔤 Icon |
| --------------- | --------------------------------------- | ---------------------------- | ------- |
| docker logs     | View logs from a container              | `docker logs myapp`          | 📜      |
| docker ps -a    | List all containers                     | `docker ps -a`               | 📋      |
| docker top      | Show running processes in a container   | `docker top myapp`           | 🧠      |
| docker events   | Real-time events from the Docker daemon | `docker events`              | 📡      |
| docker stats    | Live resource usage stats               | `docker stats`               | 📈      |
| docker exec -it | Run command inside running container    | `docker exec -it myapp bash` | 🔧      |
| docker inspect  | Detailed JSON output about resources    | `docker inspect myapp`       | 🔍      |

---

## 🛠️ Dockerfile Commands – Complete List with Explanations & Icons

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

---

## 🔥 Production-Level Commands Cheat Table with Icons

| 🔢 #   | 🛠️ Command                                  | 📘 Description                                          | ⚙️ Use-case (When/Why used)                              |
|--------|---------------------------------------------|--------------------------------------------------------|----------------------------------------------------------|
| 1️⃣    | `git clone <repo-url>`                      | 📥 Repo ko local machine pe clone karta hai            | 🔧 Jab developer kisi ek service pe kaam start karta hai |
| 2️⃣    | `git checkout -b feature/<name>`            | 🌿 New branch banata hai changes ke liye               | ✅ Production-safe code separation                        |
| 3️⃣    | `git pull origin main`                      | 🔄 Latest production/main code laata hai               | ⚠️ Merge conflict avoid karne ke liye                    |
| 4️⃣    | `git push origin feature/<name>`            | ⬆️ Apne feature branch ko push karta hai               | 🚀 Review aur CI/CD ke liye PR banane se pehle           |
| 5️⃣    | `docker-compose up -d`                      | 🐳 Services ko background me run karta hai             | 🧪 Local testing without affecting prod                  |
| 6️⃣    | `docker-compose down`                       | 🧹 Sab containers ko stop & remove karta hai           | 🚪 Local environment clean karne ke liye                 |
| 7️⃣    | `docker build -t <image-name> .`            | 🏗️ Docker image banata hai                            | 📦 Manual Docker build in CI/CD ya testing ke liye       |
| 8️⃣    | `docker push <image-name>`                  | 🚀 Docker image ko registry me bhejta hai              | 🔁 Deployment pipeline me use hota hai                   |
| 9️⃣    | `kubectl apply -f deploy.yml`               | 🧬 Kubernetes me config apply karta hai                | ☁️ Cloud deploy with versioned configs                   |
| 🔟     | `mongo` / `mongosh`                         | 🗃️ MongoDB shell open karta hai                       | 🔍 DB debug ya query testing ke liye                     |
| 1️⃣1️⃣ | `redis-cli`                                 | 🧠 Redis ke saath CLI se interact karta hai            | ⚡ Caching inspect/flush ke liye                          |
| 1️⃣2️⃣ | `kafka-console-producer.sh`                 | 📨 Kafka pe message bhejne ke liye                     | 🛠️ Kafka topic testing/dev ke liye                      |
| 1️⃣3️⃣ | `kafka-console-consumer.sh`                 | 📩 Kafka se messages read karta hai                    | 👁️ Topic monitoring and debugging                       |
| 1️⃣4️⃣ | `nginx -t`                                  | 🧪 NGINX config ka syntax test karta hai               | 🚦 Before restarting NGINX server                        |
| 1️⃣5️⃣ | `nginx -s reload`                           | 🔄 NGINX ko config changes ke baad reload karta hai    | ⚙️ Zero downtime config update ke liye                   |
| 1️⃣6️⃣ | `git merge feature/<name>`                  | 🧵 Feature branch ko main me merge karta hai           | ✅ Final QA/HR approval ke baad                           |
| 1️⃣7️⃣ | `docker logs <container-id>`                | 📋 Container logs dekhne ke liye                       | 🐞 Debugging production issues                           |
| 1️⃣8️⃣ | `docker exec -it <container> bash`          | 🧳 Container ke andar jaake kaam karne ke liye         | 🔍 Troubleshooting live containers                       |
| 1️⃣9️⃣ | `npm run build`                             | 🛠️ Production-ready JS/CSS files banata hai           | 🏗️ Frontend deploy ke liye                              |
| 2️⃣0️⃣ | `curl -X GET/POST http://localhost:port/api`| 🌐 API testing CLI se karne ke liye                    | 🔍 Endpoint check without Postman                        |
| 2️⃣1️⃣ | `git rebase main`                           | 🧬 Feature branch ko latest main ke sath sync karta hai| 🧽 Clean & linear git history                            |
| 2️⃣2️⃣ | `pm2 start app.js`                          | 🚀 Node app ko production me run karta hai             | ♻️ Process manager with auto-restart                     |
| 2️⃣3️⃣ | `pm2 logs`                                  | 📜 Real-time logs dekhne ke liye                       | 🧠 Production issue trace karne ke liye                  |
| 2️⃣4️⃣ | `pm2 restart all`                           | 🔁 All PM2 managed apps ko restart karta hai           | 🛠️ After environment config update                      |

---