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
