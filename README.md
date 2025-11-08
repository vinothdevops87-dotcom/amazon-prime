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
> cd amazon-prime

# Install dependencies
> npm install --legacy-peer-deps
> npm install react-is --legacy-peer-deps

**# Start the development server**
npm start
Once started, open 👉** http://localhost:3000**
You’ll see your Amazon Prime Clone running locally 🎬

🐳 Docker Deployment
You can easily containerize and run this project using Docker.

🧾 Dockerfile
**Dockerfile
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
docker build -t amazon-prime-clone .

▶️ Run the Container
bash
docker run -d -p 8080:80 amazon-prime-clone

Now open 👉 http://localhost:8080
Your Amazon Prime Clone app will be live! �**�

**🧰 Docker Compose (Optional)
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
docker-compose up -d
Your containerized app will now be running at http://localhost:8080**
```


## Tech Stack 💻

- React
- Redux
- Material UI
- Styled Components
- BootStrap 5
- Firebase 

## API USED ✅

- TMDB API - for getting daily high rated movies/ TV shows and searched results as per movie/ TV shows name.


## Features ✨

- Authentication process undercover with firebase and Local Storage.
- All the movie results and its details are fetched in real time using TMDB API.
- Fetches trending movie as per day selection from TMDB API, having json data of total 100 movies that are arranged in 20 movies in each category.
- Judicious use of React-YouTube & movie-trailer npm package to fetch its relevant trailer from Youtube using movie ID fetched from TMDB API.
- MUI icons with animation effects from BootStrap 5 hass been precisely used.

## Responsibilities 💪

- Team Lead in mananging & directing overall project's structure to deliver it within the deadlines.
- Landing page UI built on styled components, MUI Icons & BootStrap 5 components i.e.; Button Fade, etc.
- Login & Registration Page with implementaion of Firebase Database and LocalStorage
- Static Payment Page created using styled components and MUI icons as this project primarily focuses on front-end.
- Animation effects on movie page using BootStrap 5 i.e.; Carasouel, Popovers etc.

## Snap Shots 📷

**Home Page**

![Logo](https://images2.imgbox.com/fa/62/TCkJtA3F_o.jpg)

**Sign In**

![Logo](https://images2.imgbox.com/55/8e/f9v3aKKV_o.jpg)

**Log In**

![Logo](https://images2.imgbox.com/9e/9e/UZ4fDGvU_o.jpg)

**Payment Section**

![Logo](https://images2.imgbox.com/65/bc/20Y3bY71_o.jpg)

**Movie Page after user login**

![Logo](https://images2.imgbox.com/66/c3/v9VUf8vh_o.jpg)

**YouTube Trailer**

![Logo](https://images2.imgbox.com/9c/d8/0ZIiZwcn_o.jpg)


## References ⏩

* Icons are used from  material UI  
    https://material-ui.com/components/material-icons/
    
* Animation Effects are used from BootStrap 5  
    https://getbootstrap.com/docs/5.1/components/

* All movie and tv shows information taken  from TMDB API 
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
