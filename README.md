````markdown
# 🐾 NekoTV & NekoTV-API

**NekoTV** is a sleek, modern **anime streaming web app** built with **React + Tailwind CSS**, and **NekoTV-API** is its companion **RESTful API** for fetching anime data.  

This repository contains everything you need to **run the frontend and backend locally** or deploy your own instance.

---

## 🚩 Highlights

### NekoTV (Frontend)
- ✨ Minimal, beautiful UI powered by Tailwind CSS  
- 🔎 Search & discover anime easily  
- 📺 HD streaming for your favorite shows  
- 📌 Personal watchlist  
- 🌘 Dark mode for late-night binging  
- 📱 Fully responsive  

### NekoTV-API (Backend)
- 📂 Fetch anime details, episodes, genres, and related content  
- 🎬 Retrieve streaming servers and playable links  
- 🔍 Search anime and get suggestions  
- 📊 Trending, top airing, most popular, latest, and more  

---

## 🧩 Tech Stack

- **Frontend**: React  
- **Styling**: Tailwind CSS  
- **State Management**: Context API / Redux  
- **Backend**: Bun.js  
- **API Data Source**: [hianimez.to](https://hianimez.to) (via scraping)  

---

## ⚙️ Installation

### ✅ Prerequisites
- [Bun.js](https://bun.sh/docs/installation)  
- (Optional) [pnpm](https://pnpm.io/)  

---

### 🔧 Setup NekoTV-API (Backend)

1. Clone the repository
   ```bash
   git clone https://github.com/jsmat0m/NekoTV-API.git
   cd NekoTV-API
````

2. Install dependencies

   ```bash
   bun install
   ```

3. Start the API server

   ```bash
   bun run dev
   ```

   🚀 Running at: [http://localhost:3030](http://localhost:3030)

4. (Optional) Deploy your own instance on Render
   [![Deploy to Render](https://render.com/images/deploy-to-render-button.svg)](https://render.com/deploy?repo=https://github.com/jsmat0m/NekoTV-API)

---

### 🔧 Setup NekoTV (Frontend)

1. Clone the repository

   ```bash
   git clone https://github.com/jsmat0m/NekoTV.git
   cd NekoTV
   ```

2. Install dependencies

   ```bash
   bun install
   ```

3. Start the development server

   ```bash
   bun run dev
   ```

   🚀 Running at: [http://localhost:5173](http://localhost:5173)

---

## 🗂 Project Structure

```
NekoTV/
 ├── public/          
 ├── src/
 │   ├── components/  
 │   ├── pages/       
 │   ├── context/     
 │   ├── assets/      
 │   └── utils/       
 ├── package.json
 └── README.md

NekoTV-API/
 ├── src/
 │   ├── routes/      
 │   ├── controllers/ 
 │   ├── utils/       
 │   └── index.js     
 ├── package.json
 └── README.md
```

---

## 📚 API Documentation

### 🏠 Get Anime Home Page

```http
GET /api/v1/home
```

### 📑 Get Anime List

```http
GET /api/v1/animes/{query}/{category}?page={page}
```

Queries: `top-airing`, `most-popular`, `genre/{genre}`, `az-list/{letter}`, etc.

### 🎥 Get Anime Details

```http
GET /api/v1/anime/{animeId}
```

### 🔍 Search Anime

```http
GET /api/v1/search?keyword={query}&page={page}
GET /api/v1/search/suggestion?keyword={query}
```

### 🎞️ Episodes

```http
GET /api/v1/episodes/{animeId}
```

### 🌐 Episode Servers

```http
GET /api/v1/servers?id={episodeId}
```

### ▶️ Streaming Links

```http
GET /api/v1/stream?id={episodeId}&server={server}&type={sub|dub}
```

---

## 🛣 Roadmap

* ✅ Core streaming & API functionality
* ✅ Dark/light mode
* ⏳ User authentication & profiles
* ⏳ Offline watchlist support
* ⏳ Multi-language support

---

## 🤝 Contributing

1. Fork the repository
2. Create a branch (`git checkout -b feature-branch`)
3. Make changes & commit (`git commit -m "Add feature"`)
4. Push & create a pull request

---

## ✨ Contributors

[![](https://contrib.rocks/image?repo=jsmat0m/NekoTV-API)](https://github.com/jsmat0m/NekoTV-API/graphs/contributors)

---

## 🙏 Thanks

* [consumet.ts](https://github.com/consumet/consumet.ts)
* [api.consumet.org](https://github.com/consumet/api.consumet.org)

---

## ⭐ Support

If you like this project, **leave a star** 🌟 on GitHub!

---

```


