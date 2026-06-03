# 💬 TalkyTalk — Real-Time Chat App

> A full-stack MERN chat application with real-time messaging, group chats, and user authentication — built with Socket.io for instant communication.

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Socket.io](https://img.shields.io/badge/Socket.io-010101?style=flat-square&logo=socketdotio&logoColor=white)

---

## ✨ Features

| Feature | Description |
|---|---|
| 🔐 Authentication | Secure sign up / login with JWT & bcrypt password hashing |
| 💬 Real-time Messaging | Instant message delivery via Socket.io WebSockets |
| 👥 Group Chats | Create groups, add/remove members, rename groups |
| 🔍 User Search | Find and start conversations with any registered user |
| ☁️ Image Uploads | Profile picture uploads via Cloudinary |
| 🟢 Online Status | See who's currently online in real time |

---

## 🛠️ Tech Stack

**Frontend**
- React — UI components and state management
- Axios — HTTP requests to the backend API
- Socket.io-client — WebSocket connection for real-time events
- Chakra UI — Component library for styling

**Backend**
- Node.js + Express — REST API server
- MongoDB + Mongoose — Database and schema modeling
- Socket.io — WebSocket server for real-time messaging
- JWT — Stateless authentication tokens
- bcrypt — Password hashing
- Cloudinary — Cloud image storage

---

## 🚀 Quick Start

### Prerequisites
- Node.js v16+
- MongoDB (local or Atlas)
- Cloudinary account

### 1. Clone the repository
```bash
git clone https://github.com/divyansheeverma/talky-talk.git
cd talky-talk
```

### 2. Set up environment variables

Create a `.env` file in the `/backend` directory:
```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
```

### 3. Install & run

```bash
# Install backend dependencies
cd backend
npm install
npm start

# Install frontend dependencies (new terminal)
cd frontend
npm install
npm start
```

App runs at `http://localhost:3000`

---

## 📁 Project Structure

```
talky-talk/
├── frontend/
│   ├── src/
│   │   ├── components/       # Chat, Sidebar, MessageBox UI
│   │   ├── context/          # Socket & Auth context providers
│   │   ├── pages/            # Login, Register, Chat pages
│   │   └── App.js
│   └── package.json
│
├── backend/
│   ├── controllers/          # Auth, chat, message logic
│   ├── models/               # User, Chat, Message schemas
│   ├── routes/               # API route definitions
│   ├── middleware/            # JWT auth middleware
│   ├── config/               # DB connection, Cloudinary config
│   └── server.js
│
└── README.md
```

---

## 🔌 API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| `POST` | `/api/user/register` | Register new user |
| `POST` | `/api/user/login` | Login & receive JWT |
| `GET` | `/api/user?search=` | Search users by name |
| `POST` | `/api/chat` | Create / access 1-on-1 chat |
| `GET` | `/api/chat` | Fetch all chats for user |
| `POST` | `/api/chat/group` | Create a group chat |
| `GET` | `/api/message/:chatId` | Fetch messages for a chat |
| `POST` | `/api/message` | Send a new message |

---

## ⚡ Real-Time Events (Socket.io)

```
Client connects → joins personal room
User sends message → server emits to all chat members
Typing indicator → broadcast to chat room
User goes offline → online status updated
```

## 🤝 Contributing

Feel free to fork and submit PRs. Open an issue for any bugs or feature requests.

---

## 📄 License

MIT License

---

*Built with the MERN stack & Socket.io · by [Divyanshee Verma](https://github.com/divyansheeverma)*
