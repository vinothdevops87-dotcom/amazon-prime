# 🎬 Amazon Prime Video - Clone

Amazon Prime Video is an American subscription-based on-demand streaming platform by Amazon.  
This project is a **front-end clone** built to replicate its core UI and functionality for learning and demonstration purposes.

> 🧑‍💻 A collaborative project built by a team of 3 developers in **7 days**.

---

## 🚀 Demo

**Live Preview:** [Enjoy the Experience](https://amazonprime-clone.netlify.app/)

---

## ⚙️ Local Setup and Docker Deployment

### 🧠 Local Setup (Test on your system)

```bash
# Clone the repository
git clone https://github.com/vinothdevops87-dotcom/amazon-prime.git

# Navigate into the project directory
cd amazon-prime

# Install dependencies
npm install --legacy-peer-deps
npm install react-is --legacy-peer-deps

# Start the development server
npm start
Once started, open 👉 http://localhost:3000
You’ll see your Amazon Prime Clone running locally 🎬

🐳 Docker Deployment
You can easily containerize and run this project using Docker.

🧾 Dockerfile
Dockerfile
Copy code
# ---------- Build Stage ----------
FROM node:18-alpine AS build
WORKDIR /app
COPY package*.json ./
RUN npm install --legacy-peer-deps
COPY . .
RUN npm run build
CMD ["npm", "start"]

# ---------- Production Stage ----------
FROM nginx:alpine
COPY --from=build /app/build /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
🏗️ Build the Docker Image
bash
Copy code
docker build -t amazon-prime-clone .
▶️ Run the Container
bash
Copy code
docker run -d -p 8080:80 amazon-prime-clone
Now open 👉 http://localhost:8080
Your Amazon Prime Clone app will be live! 🎉

🧰 Docker Compose (Optional)
You can also use Docker Compose for easier setup and container management.

yaml
Copy code
version: "3"
services:
  app:
    build: .
    ports:
      - "8080:80"
    container_name: amazon-prime-clone
🚀 Run the app
bash
Copy code
docker-compose up -d
Your containerized app will now be running at http://localhost:8080

🧩 Table of Contents
Project Overview

Tech Stack

API Used

Features

Responsibilities

Snapshots

References

Contributors

📝 Project Overview
This project demonstrates the UI, authentication, and movie data integration of Amazon Prime Video using React.
It connects to the TMDB API for fetching real-time movie and TV show data, and uses Firebase for authentication.

💻 Tech Stack
⚛️ React.js

🔁 Redux

🎨 Material-UI

💅 Styled Components

🅱️ Bootstrap 5

🔥 Firebase

✅ API Used
TMDB API — For fetching trending movies, TV shows, and search results.
https://developers.themoviedb.org/3

✨ Features
🔐 User Authentication with Firebase & LocalStorage

🎞️ Trending Movies and TV Shows from TMDB

▶️ YouTube Trailers integrated using react-youtube

🎨 Material UI Icons and Bootstrap animations

⚡ Dynamic Movie Pages and Static Payment Page

🧩 Component-based architecture for modular structure

💪 Responsibilities
👨‍💻 Team Lead — Managed project structure and deadlines

🖼️ Built Landing Page UI using MUI, Styled Components & Bootstrap

🔑 Developed Login and Registration with Firebase integration

💳 Created Static Payment Page using MUI & Styled Components

🎬 Implemented Carousel & Animation Effects on movie pages

📸 Snapshots
🏠 Home Page


🔑 Sign In


🔓 Log In


💳 Payment Section


🎥 Movie Page


▶️ YouTube Trailer


📚 References
🎨 Material UI Icons

🌀 Bootstrap 5 Components

🎬 TMDB API

▶️ React YouTube Package

👥 Contributors
👤 Biswaranjan — Team Lead

👤 Rajan Kumar

👤 Abhijeet Sinha

👤 Vinoth Kumar — Docker & Deployment