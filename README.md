# TypeBrawl

A **real-time multiplayer typing battle** game inspired by MonkeyType, featuring **low-latency WebSocket synchronization**, a **live leaderboard**, and **anti-cheat mechanisms**. The system uses **Redis for caching & pub/sub events**, **PostgreSQL for persistent data**, and **React + WebSockets for a smooth frontend experience**.

---

## 🚀 Features
✅ **Real-Time Multiplayer Battles** – Instant input tracking using WebSockets  
✅ **Live Leaderboard** – Updates every second via Redis  
✅ **Dynamic Prompt Generation** – AI-generated or pre-stored texts  
✅ **Fair Gameplay & Anti-Cheat** – Detects unnatural typing speeds  
✅ **Reconnect Support** – Players can resume mid-game  
✅ **Global Deployment** – Low-latency performance using Redis & WebSockets  

---

## 🛠 Tech Stack

### **Frontend:**
- **React (Vite) + Tailwind CSS** – Responsive UI
- **Native WebSockets (WebSocket API)** – Real-time updates
- **Web Workers** – Offload intensive WPM calculations
- **Service Workers** – Background sync & offline support

### **Backend:**
- **Node.js (uWebSockets.js or Fastify)** – High-performance WebSocket server
- **Redis (Pub/Sub & Leaderboards)** – Ultra-fast real-time updates
- **PostgreSQL (pg module)** – Persistent storage for game history
- **Kafka** – Event-driven architecture for analytics

### **Infrastructure & Scaling:**
- **Docker + Kubernetes** – Containerized deployment
- **Cloudflare (WebSocket Proxying)** – Reduce latency globally
- **AWS (EC2)** – Scalable backend hosting
- **Redis Cluster + Sentinel** – High-availability caching

---

## 📂 Folder Structure
```
/TypeBrawl
│── backend/                # Node.js WebSocket Server  
│   ├── src/
│   │   ├── controllers/    # Game logic & matchmaking  
│   │   ├── services/       # Prompt generation, leaderboard handling  
│   │   ├── utils/          # Rate limiting, anti-cheat checks  
│   │   ├── database.js     # Raw PostgreSQL (pg module) connection  
│   │   ├── redis.js        # Redis connection  
│   │   ├── index.js        # WebSocket server  
│   ├── Dockerfile          
│── frontend/               # React Client  
│   ├── src/  
│   │   ├── components/     # UI components  
│   │   ├── hooks/          # WebSocket & state management  
│   │   ├── pages/          # Game UI, leaderboard  
│   ├── package.json  
│   ├── Dockerfile  
│── docker-compose.yml      # Redis + PostgreSQL setup  
│── README.md  
```

---

## 🔧 Setup Instructions

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/yourusername/TypeBrawl.git
cd TypeBrawl
```

### 2️⃣ Start Backend
```bash
cd backend
npm install
npm start
```

### 3️⃣ Start Frontend
```bash
cd frontend
npm install
npm run dev
```

### 4️⃣ Run Redis & PostgreSQL (Docker)
```bash
docker-compose up -d
```

---

## 📝 Roadmap
- [ ] Implement WebRTC for lower-latency communication  
- [ ] Add AI-generated typing prompts  
- [ ] Introduce ranking & competitive matchmaking  

---

## 📜 License
MIT

---

