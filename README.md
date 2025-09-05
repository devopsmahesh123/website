# Anon - An eCommerce Website

![GitHub repo size](https://img.shields.io/github/repo-size/codewithsadee/anon-ecommerce-website)
![GitHub stars](https://img.shields.io/github/stars/codewithsadee/anon-ecommerce-website?style=social)
![GitHub forks](https://img.shields.io/github/forks/codewithsadee/anon-ecommerce-website?style=social)
[![Twitter Follow](https://img.shields.io/twitter/follow/codewithsadee_?style=social)](https://twitter.com/intent/follow?screen_name=codewithsadee_)
[![YouTube Video Views](https://img.shields.io/youtube/views/3l8Lob4ysI0?style=social)](https://youtu.be/3l8Lob4ysI0)

Anon is a fully responsive ecommerce website, maximum compatiblities in all mobile devices, built using HTML, CSS, and JavaScript.

## Demo new

![Anon Desktop Demo](./website-demo-image/desktop.png "Desktop Demo")
![Anon Mobile Demo](./website-demo-image/mobile.png "Mobile Demo")


Perfect, Sadeeq! That repo hosts **Anon**, a responsive eCommerce website built with **HTML, CSS, and JavaScript**—no backend, so it's ideal for static hosting behind NGINX.

Here’s how you can deploy it on **EC2 with Docker and NGINX**:

---

## 🛠️ Step-by-Step: Deploy Anon Website on EC2 with Docker + NGINX

### 1️⃣ **SSH into EC2**
```bash
ssh -i your-key.pem ubuntu@your-ec2-ip
```

---

### 2️⃣ **Install Docker**
```bash
sudo apt update
sudo apt install -y docker.io
sudo systemctl start docker
sudo systemctl enable docker
```

---

### 3️⃣ **Clone the Repo**
```bash
git clone https://github.com/devopsmahesh123/website.git
cd website
```

---

### 4️⃣ **Create Dockerfile**
```bash
nano Dockerfile
```

Paste this:
```Dockerfile
FROM nginx:alpine
COPY . /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
```

---

### 5️⃣ **Build Docker Image**
```bash
docker build -t anon-ecommerce .
```

---

### 6️⃣ **Run Container**
```bash
docker run -d --name anon-site -p 80:80 anon-ecommerce
```

---

### ✅ **Access the Site**
Open your browser and visit:
```
http://<your-ec2-public-ip>
```

You should see the Anon homepage in all its responsive glory.

---
