# 🐳 Docker Nginx Web Server

This is a simple static website served using **Nginx inside a Docker container**. It demonstrates how to containerize a basic HTML website.

---

## 📁 Project Structure

```
WebServerDocker/
├── Dockerfile
├── index.html
└── README.md
```

---

## 🚀 What This Project Does

* Uses official `nginx:alpine` Docker image
* Copies a custom `index.html` into the Nginx web root
* Runs a lightweight web server inside a container
* Exposes the website on a local port

---

## 🛠️ Build the Docker Image

Run this command inside the project folder:

```bash
docker build -t my-web-server .
```

---

## ▶️ Run the Container

```bash
docker run -d -p 5000:80 --name mywebsite my-web-server
```

---

## 🌐 Access the Website

Open your browser and go to:

```
http://localhost:5000
```

You should see your custom HTML page served by Nginx.

---

## 📄 Stop the Container

```bash
docker stop mywebsite
```

---

## 🗑️ Remove the Container

```bash
docker rm mywebsite
```

---

## 🔁 Rebuild After Changes

If you update `index.html`, rebuild the image:

```bash
docker build --no-cache -t my-web-server .
```

Then rerun the container.

---

## ⚙️ Notes

* Nginx serves files from:

  ```
  /usr/share/nginx/html
  ```
* Default container port is **80**
* Host port (5000 in this case) can be changed freely

Example:

```bash
docker run -d -p 8080:80 my-web-server
```

---

## 📌 Technologies Used

* Docker 🐳
* Nginx 🌐
* HTML
