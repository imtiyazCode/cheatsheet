# 🐳 Docker Cheatsheet

> Learn Docker with simple explanations and commonly used commands.

---

## 📌 What is Docker?

Docker helps you run apps in **containers**, which are like lightweight virtual machines. Each container has everything your app needs code, tools, libraries so it works the same everywhere.

---

## 🔧 Basic Commands

### ✅ Check if Docker is installed
```bash
docker --version
docker info
````

### 🆘 Need help?

```bash
docker --help
docker <command> --help
```

---

## 📥 Downloading Images

Images are the "blueprints" for containers.

```bash
docker pull ubuntu         # Get Ubuntu image from Docker Hub
docker pull node:18-alpine # Get Node.js lightweight image
```

---

## 🚀 Running Containers

A container is like a running app based on an image.

```bash
docker run ubuntu                  # Run Ubuntu container
docker run -it ubuntu bash         # Run and open terminal in it
docker run -d nginx                # Run nginx in background (detached)
docker run -p 3000:3000 my-app     # Map container port to your computer
docker run --name mycontainer ubuntu  # Give a custom name
```

---

## 📂 Stopping and Removing Containers

```bash
docker ps                  # Show running containers
docker ps -a               # Show all containers (even stopped)
docker stop <name_or_id>   # Stop a container
docker rm <name_or_id>     # Delete a container
```

---

## 🖼️ Working with Images

```bash
docker images              # Show downloaded images
docker rmi <image_id>      # Remove an image
```

---

## 🛠️ Build Your Own Image (with Dockerfile)

```bash
docker build -t my-app .   # Build image in current folder
```

📝 Example Dockerfile:

```Dockerfile
FROM node:18-alpine
WORKDIR /app
COPY . .
RUN npm install
CMD ["npm", "start"]
```

---

## 🧪 Run Commands in a Container

```bash
docker exec -it <name_or_id> bash    # Open terminal in a running container
docker exec <name_or_id> ls          # Run a command like 'ls'
```

---

## 📁 Volumes – Save Data

Volumes help keep your data even if the container is deleted.

```bash
docker volume create my-volume
docker run -v my-volume:/app/data ubuntu
```

---

## 🌐 Networks – Connect Containers

```bash
docker network ls                    # List networks
docker network create my-network    # Create new network
docker network connect my-network <container>
```

---

## 🧹 Cleaning Up

```bash
docker stop $(docker ps -q)      # Stop all running containers
docker rm $(docker ps -aq)       # Remove all containers
docker rmi $(docker images -q)   # Remove all images
docker system prune              # Clean up unused stuff
```

---

## 🧬 Docker Compose (Multiple Containers)

If your app has multiple services (e.g., Node + MongoDB), use `docker-compose.yml`.

```bash
docker-compose up       # Start everything
docker-compose down     # Stop and remove everything
```

Example `docker-compose.yml`:

```yaml
version: "3"
services:
  web:
    build: .
    ports:
      - "3000:3000"
  mongo:
    image: mongo
```

---

## ✅ Common Flags (Options)

| Flag   | What it does                   |
| ------ | ------------------------------ |
| `-d`   | Run in background (detached)   |
| `-p`   | Port mapping                   |
| `-v`   | Volume mount                   |
| `--rm` | Delete container after exit    |
| `-it`  | Interactive mode with terminal |

---

## 📚 Useful Resources

* 📘 [Official Docker Docs](https://docs.docker.com/)
* 🐙 [Docker Hub](https://hub.docker.com/)
* 💡 [Play with Docker (online)](https://labs.play-with-docker.com/)

---

> ✨ **Tip for Beginners**: Start by running existing images (like `nginx` or `ubuntu`) to get comfortable. Then try building your own container step-by-step!

---

## 🧑‍💻 Author

**Imtiyaz Nandasaniya**  
* [GitHub: @imtiyazCode](https://github.com/imtiyazCode)
* [Instagram: @code.clash](https://instagram.com/code.clash)

---

## ⭐️ Found this useful?

Give this repo a star and help others discover it too!
