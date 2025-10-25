# 🎬 DisneyClone — Netflix-Style Streaming App

A **Netflix-style clone** built with **React + Vite (Frontend)** and **Node.js + Express + MongoDB (Backend)**.  
Designed as a full-stack learning project during internship — featuring TMDB movie APIs, Firebase authentication, and modern UI design.

---

## ✨ Overview

> 🎥 _“Stream. Discover. Experience.”_

DisneyClone delivers a sleek, responsive UI that mimics the Netflix interface — complete with movie carousels, authentication, and dynamic trailer fetching from TMDB API.

---

## 🚀 Features

✅ Responsive and modern UI with hero banners and hover effects  
✅ TMDB integration for real-time movie data and trailers  
✅ User authentication with Firebase (Signup/Login/Logout)  
✅ Node.js backend with Express routing and MongoDB  
✅ Component-based React structure for scalability

---

## 🧩 Tech Stack

| Area                    | Technologies                       |
| ----------------------- | ---------------------------------- |
| 🎨 **Frontend**         | React 18, Vite, Axios, CSS Modules |
| 🧠 **State Management** | React Context API (Auth Context)   |
| 🔒 **Authentication**   | Firebase (Email/Password)          |
| 🧾 **Backend**          | Node.js, Express.js, Mongoose      |
| 🗄️ **Database**         | MongoDB Atlas                      |
| 🎬 **API**              | TMDB (The Movie Database)          |

---

## 🗂️ Folder Structure (Simplified)

```

DisneyClone/
│
├── Backend/
│   ├── entry.mjs
│   ├── database.mjs
│   ├── Controller/
│   │   ├── Movies.Controller.mjs
│   │   └── User.Controller.mjs
│   ├── Models/
│   │   ├── Movies.mjs
│   │   └── Client.mjs
│   └── Routes/
│       ├── MoviesRoutes.mjs
│       └── UserRoutes.mjs
│
├── src/
│   ├── main.jsx
│   ├── App.jsx
│   ├── AuthContext.jsx
│   ├── Firebase.js
│   ├── Components/
│   │   ├── Navbar/
│   │   ├── Footer/
│   │   └── TitleCards/
│   └── Pages/
│       ├── Login/
│       ├── Home/
│       └── Player/
│
├── vite.config.js
└── package.json

```

---

## ⚙️ Setup & Installation

### 🧰 Requirements

- Node.js (v14+)
- npm or yarn
- MongoDB (local or cloud)

### 🪄 Steps

```bash
# 1️⃣ Clone repository
git clone <repo-url>
cd DisneyClone

# 2️⃣ Install frontend dependencies
npm install

# 3️⃣ Install backend dependencies
cd Backend
npm install

# 4️⃣ Start backend server
npm start  # runs entry.mjs (default: port 1000)

# 5️⃣ Start frontend
cd ..
npm run dev  # default: http://localhost:5173
```

---

## 🔑 Environment Variables

Create a `.env` file in the `Backend/` directory with:

```
MONGO_URI=<your_mongo_connection_string>
TMDB_API_KEY=<your_tmdb_api_key>
PORT=1000
```

For Firebase (Frontend):

```
VITE_FIREBASE_API_KEY=<your_firebase_key>
VITE_FIREBASE_AUTH_DOMAIN=<your_auth_domain>
```

_(⚠️ Don’t commit your .env files!)_

---

## 🧠 Key Components & Files

| Area                   | File                                                                                   | Description                 |
| ---------------------- | -------------------------------------------------------------------------------------- | --------------------------- |
| 🎬 **Frontend Entry**  | [`src/main.jsx`](src/main.jsx)                                                         | Vite main entry point       |
| 🧭 **Router/App**      | [`src/App.jsx`](src/App.jsx)                                                           | Defines routes & pages      |
| 🔑 **Auth Context**    | [`src/AuthContext.jsx`](src/AuthContext.jsx)                                           | Handles Firebase auth state |
| 🧱 **Firebase Config** | [`src/Firebase.js`](src/Firebase.js)                                                   | Contains Firebase helpers   |
| 🗄️ **Backend Entry**   | [`Backend/entry.mjs`](Backend/entry.mjs)                                               | Starts Express server       |
| 🎞️ **Movies API**      | [`Backend/Controller/Movies.Controller.mjs`](Backend/Controller/Movies.Controller.mjs) | TMDB data fetcher           |
| 👤 **User API**        | [`Backend/Controller/User.Controller.mjs`](Backend/Controller/User.Controller.mjs)     | Handles user signup/login   |

---

## 💻 Common Commands

| Task               | Command                   |
| ------------------ | ------------------------- |
| Run frontend       | `npm run dev`             |
| Build production   | `npm run build`           |
| Preview production | `npm run preview`         |
| Lint code          | `npm run lint`            |
| Run backend        | `cd Backend && npm start` |

---

## 🧭 Usage Example

- Open the app → `http://localhost:5173`
- Sign in via Firebase (Login Page `/`)
- Explore movies on `/home` (dynamic carousels)
- Click a movie → `/Player/:id` page fetches and plays trailer via backend TMDB route

---

## 🧩 Future Improvements

- 🌍 Add multi-language support
- 🔐 JWT-based authentication (backend)
- 🧱 Centralized `.env` config
- 🧠 Recommendation system (content-based filtering)
- 📱 PWA (Progressive Web App) support

---

## 🤝 Contributing

1. **Fork** the repository
2. Create a **feature branch** (`git checkout -b feature/your-feature`)
3. **Commit** your changes with clear messages
4. **Push** to your branch and open a **Pull Request**

---

## 📜 License

Licensed under the **MIT License** — feel free to use for learning and portfolio purposes.

---

## 👨‍💻 Author

**Kashif Zulifqar**
📧 Email: [bhuttokashifali957@gmail.com](mailto:bhuttokashifali957@gmail.com)
💼 [LinkedIn](<(https://www.linkedin.com/in/kashif-zulifqar-1856aa2b2)>) | 🐙 [GitHub](https://github.com/Kashif-Zulifqar)

---

⭐ _If you like this project, don’t forget to give it a star!_ ⭐

```


```
