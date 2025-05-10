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

# 🚀 React Native TypeScript Project Setup

Welcome to your React Native project! Follow these clean and organized steps to install all necessary dependencies and configure the environment properly.

---

## 📦 Install Dependencies (One-by-One)

```bash
npm install @react-native-async-storage/async-storage
```
```bash
npm install @react-native-clipboard/clipboard
```
```bash
npm install @react-native-community/blur
```
```bash
npm install @react-navigation/bottom-tabs
```
```bash
npm install @react-navigation/native
```
```bash
npm install @react-navigation/native-stack
```
```bash
npm install @reduxjs/toolkit
```
```bash
npm install @types/react-native
```
```bash
npm install axios
```
```bash
npm install d3-shape
```
```bash
npm install expo-av
```
```bash
npm install formik
```
```bash
npm install i18next
```
```bash
npm install lottie-react-native
```
```bash
npm install react
```
```bash
npm install react-i18next
```
```bash
npm install react-native
```
```bash
npm install react-native-confetti-cannon
```
```bash
npm install react-native-dotenv
```
```bash
npm install react-native-gesture-handler
```
```bash
npm install react-native-get-random-values
```
```bash
npm install react-native-haptic-feedback
```
```bash
npm install react-native-keyboard-aware-scroll-view
```
```bash
npm install react-native-linear-gradient
```
```bash
npm install react-native-localize
```
```bash
npm install react-native-mmkv
```
```bash
npm install react-native-reanimated
```
```bash
npm install react-native-reanimated-carousel
```
```bash
npm install react-native-reanimated-numbers
```
```bash
npm install react-native-responsive-fontsize
```
```bash
npm install react-native-rolling-bar
```
```bash
npm install react-native-safe-area-context
```
```bash
npm install react-native-screens
```
```bash
npm install react-native-snap-carousel
```
```bash
npm install react-native-sound
```
```bash
npm install react-native-svg
```
```bash
npm install react-native-svg-transformer
```
```bash
npm install react-native-switch
```
```bash
npm install react-native-unistyles
```
```bash
npm install react-native-vector-icons
```
```bash
npm install react-native-video
```
```bash
npm install react-native-wheel-of-fortune
```
```bash
npm install react-redux
```
```bash
npm install redux-persist
```
```bash
npm install uuid
```
```bash
npm install yup
```
```bash
npm install zustand
```

```bash
npm install --save-dev @babel/core @babel/preset-env @babel/preset-typescript babel-jest
```
---

## 🧰 Expo Native Dependencies (If Using Expo)

```bash
npx expo install react-native-gesture-handler react-native-reanimated react-native-screens react-native-safe-area-context react-native-svg
```

---

## 🍎 iOS CocoaPods (For Non-Expo iOS Projects)

```bash
npx pod-install
```

---

## ⚙️ Reanimated Configuration

**Import in Entry File (e.g., `index.tsx`)**

```js
import 'react-native-reanimated';
```

**babel.config.js Setup**

```js
module.exports = {
  presets: ['module:metro-react-native-babel-preset'],
  plugins: [
    // Other plugins
    'react-native-reanimated/plugin',
  ],
};
```

# 👨‍💻 100% Computer Science Engineer Deep Dive (Kaushik's Ultimate Guide)

Welcome to the most practical + complete 🔥 Computer Science Engineering Knowledge Repo — designed by Kaushik, for Kaushik. Hinglish mein samjha gaya hai, real-world job ke hisaab se sorted hai 👇

---

## 📚 Table of Contents

- [🚀 React Native TypeScript Project Setup](#-react-native-typescript-project-setup)
  - [📦 Install Dependencies (One-by-One)](#-install-dependencies-one-by-one)
  - [🧰 Expo Native Dependencies (If Using Expo)](#-expo-native-dependencies-if-using-expo)
  - [🍎 iOS CocoaPods (For Non-Expo iOS Projects)](#-ios-cocoapods-for-non-expo-ios-projects)
  - [⚙️ Reanimated Configuration](#️-reanimated-configuration)
- [👨‍💻 100% Computer Science Engineer Deep Dive (Kaushik's Ultimate Guide)](#-100-computer-science-engineer-deep-dive-kaushiks-ultimate-guide)
  - [📚 Table of Contents](#-table-of-contents)
  - [⚙️ Operating Systems](#️-operating-systems)
  - [🧵 Computer Networks](#-computer-networks)
  - [💾 DBMS](#-dbms)
  - [🔒 Cybersecurity](#-cybersecurity)
  - [🧮 Compiler Design](#-compiler-design)
  - [🔢 Discrete Mathematics](#-discrete-mathematics)
  - [💡 Digital Electronics](#-digital-electronics)
  - [🧾 Automata Theory](#-automata-theory)
  - [🧪 Software Testing](#-software-testing)
  - [📦 Software Engineering](#-software-engineering)
  - [⚛️ Design Patterns](#️-design-patterns)
  - [🧰 Tools and IDEs](#-tools-and-ides)
  - [🧱 Version Control](#-version-control)
  - [☁️ Cloud and Deployment](#️-cloud-and-deployment)
  - [🛡️ Data Privacy](#️-data-privacy)
  - [🌐 Web Protocols](#-web-protocols)
  - [🔄 Event Loop and Concurrency](#-event-loop-and-concurrency)
  - [⚗️ API Design](#️-api-design)
  - [📈 Complexity](#-complexity)
  - [🧠 LLD (Low Level Design)](#-lld-low-level-design)
  - [🏗️ HLD (High Level Design)](#️-hld-high-level-design)
  - [🧩 Middleware](#-middleware)
  - [👾 Emulator vs Simulator](#-emulator-vs-simulator)
  - [🎛️ Configuration Management](#️-configuration-management)
  - [🤖 AI Ethics](#-ai-ethics)
  - [📊 Business + Tech](#-business--tech)
  - [🧑‍💻 Backend Developer Roadmap](#-backend-developer-roadmap)
  - [❤️ Made with love by Kaushik](#️-made-with-love-by-kaushik)

---

## ⚙️ Operating Systems
- 🔹 Process vs Thread
- 🔹 Context Switching
- 🔹 Memory Management (Heap/Stack)
- 🔹 Virtual Memory, Paging
- 🔹 Scheduling Algorithms (FCFS, RR, SJF)
- 🔹 Deadlock Conditions + Banker's Algorithm

## 🧵 Computer Networks
- 🔹 OSI vs TCP/IP Layers
- 🔹 HTTP vs HTTPS
- 🔹 IP Addressing, Subnetting
- 🔹 DNS, DHCP, NAT
- 🔹 WebSockets, TCP/UDP

## 💾 DBMS
- 🔹 ER Diagrams, Relationships
- 🔹 Indexing, Views, Triggers
- 🔹 Transactions, ACID Properties
- 🔹 Normalization (1NF–3NF, BCNF)
- 🔹 SQL Joins (Inner, Left, Right, Full)

## 🔒 Cybersecurity
- 🔹 OWASP Top 10
- 🔹 HTTPS, TLS, SSL
- 🔹 JWT, OAuth2, CORS
- 🔹 SQL Injection, XSS
- 🔹 Hashing (SHA, Bcrypt), Encryption (AES, RSA)

## 🧮 Compiler Design
- 🔹 Tokenization, Lexical Analysis
- 🔹 Syntax Tree, Grammar
- 🔹 Parser Types (LL, LR)
- 🔹 Intermediate Code Generation

## 🔢 Discrete Mathematics
- 🔹 Set Theory, Relations
- 🔹 Graph Theory, Trees
- 🔹 Propositional Logic
- 🔹 Permutations, Combinations
- 🔹 Boolean Algebra

## 💡 Digital Electronics
- 🔹 Binary, Octal, Hex
- 🔹 Logic Gates (AND, OR, XOR, NAND)
- 🔹 Flip-Flops, Multiplexers
- 🔹 Counters, Registers

## 🧾 Automata Theory
- 🔹 DFA, NFA
- 🔹 CFG (Context Free Grammar)
- 🔹 Turing Machines
- 🔹 Regular Expressions

## 🧪 Software Testing
- 🔹 Unit Testing (Jest, Pytest, JUnit)
- 🔹 Integration Testing
- 🔹 Manual vs Automated Testing
- 🔹 TDD / BDD

## 📦 Software Engineering
- 🔹 SDLC Models (Agile, Waterfall)
- 🔹 Requirements Analysis
- 🔹 SRS, UML, Use Cases

## ⚛️ Design Patterns
- 🔹 Singleton, Factory
- 🔹 Strategy, Adapter
- 🔹 Observer, Proxy

## 🧰 Tools and IDEs
- 🔹 VSCode, IntelliJ, PyCharm
- 🔹 Postman, Docker, Figma
- 🔹 Firebase, JIRA, GitHub

## 🧱 Version Control
- 🔹 Git Basics, Branching
- 🔹 PR Flow, Merge Conflicts
- 🔹 Git Hooks

## ☁️ Cloud and Deployment
- 🔹 AWS EC2, S3, Route 53
- 🔹 Firebase Hosting
- 🔹 CI/CD Pipelines
- 🔹 NGINX, Docker Compose

## 🛡️ Data Privacy
- 🔹 GDPR Basics
- 🔹 Cookies, User Consent
- 🔹 Data Collection Limits

## 🌐 Web Protocols
- 🔹 HTTP Methods, Status Codes
- 🔹 MIME Types, Headers
- 🔹 WebSockets, Caching

## 🔄 Event Loop and Concurrency
- 🔹 JS Event Loop, Call Stack
- 🔹 Promises, async/await
- 🔹 Threading, Workers

## ⚗️ API Design
- 🔹 REST vs GraphQL
- 🔹 OpenAPI Spec
- 🔹 Versioning, Pagination

## 📈 Complexity
- 🔹 Time/Space Tradeoffs
- 🔹 Big O Analysis (All Cases)
- 🔹 Recursion Tree, DP Table

## 🧠 LLD (Low Level Design)
- 🔹 Class Diagrams
- 🔹 OOPS Deep Dive
- 🔹 Object Modeling (UML)

## 🏗️ HLD (High Level Design)
- 🔹 Scalable Architecture
- 🔹 Load Balancer, CDN
- 🔹 Queue System (Kafka, RabbitMQ)

## 🧩 Middleware
- 🔹 Redis Pub/Sub
- 🔹 Kafka Streams
- 🔹 RabbitMQ Queues

## 👾 Emulator vs Simulator
- 🔹 Real Devices vs Virtual
- 🔹 Debugging & Logs

## 🎛️ Configuration Management
- 🔹 Ansible, Helm, Chef
- 🔹 Environment Variables

## 🤖 AI Ethics
- 🔹 Bias, Explainability
- 🔹 Consent Based Datasets

## 📊 Business + Tech
- 🔹 CAC, LTV, Burn Rate
- 🔹 SaaS Metrics, Retention
- 🔹 Tech + Product Fit

## 🧑‍💻 Backend Developer Roadmap
- 🔹 Core Programming (JS, Python, Go, TS, Java)
- 🔹 Web Servers (Express.js, FastAPI, Spring Boot)
- 🔹 Databases (SQL + NoSQL)
- 🔹 Authentication (JWT, OAuth2, Sessions)
- 🔹 Caching (Redis)
- 🔹 Queues (RabbitMQ, Kafka)
- 🔹 File Storage (S3, Local, Cloudinary)
- 🔹 API Design (REST, GraphQL)
- 🔹 Docker + Containers
- 🔹 NGINX, Load Balancer
- 🔹 CI/CD Pipelines
- 🔹 Logs & Monitoring (Prometheus, Grafana, ELK)
- 🔹 Security Best Practices
- 🔹 Deployment (AWS, DigitalOcean, Railway)

---

Want to contribute or track your learning here? Make a Fork or Star ⭐

📬 Connect: kaushik@curoster.com


---

## ❤️ Made with love by Kaushik

> The best code starts with passion and ends with perfection.