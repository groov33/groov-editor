# ⚡ Real-Time Collaborative Code Editor

[![Live Demo](https://img.shields.io/badge/Live_Demo-Visit_Editor-0070F3?style=for-the-badge&logo=vercel&logoColor=white)](https://groov-editor.vercel.app)
[![Author](https://img.shields.io/badge/Author-Ayush_Pandey-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/groov33)
[![Tech Stack](https://img.shields.io/badge/Stack-React_|_CodeMirror_|_Node.js_|_Socket.IO_|_WebSockets-22C55E?style=for-the-badge)](https://github.com/groov33/groov-editor)

> A high-performance, synchronized collaborative coding environment enabling multiple developers to write, edit, and inspect code concurrently in real-time rooms.

---

## 🌐 Live Deployments
* **Frontend Web App:** [https://groov-editor.vercel.app](https://groov-editor.vercel.app)
* **WebSocket Backend Server:** [https://groov-editor-server.onrender.com](https://groov-editor-server.onrender.com)

---

## 📌 Project Overview
Developed as a flagship systems & full-stack resume project showcasing bidirectional WebSocket protocols, distributed client state synchronization, and reactive UI architecture. Developers can instantly generate unique room identifiers, invite peers, and pair-program simultaneously with zero latency and conflict-free text updates.

### ✨ Key Features
- **Real-Time Code Synchronization:** Built with Socket.IO and WebSocket protocols to broadcast character-level code changes instantaneously across all connected room participants.
- **Interactive CodeMirror IDE:** Embedded CodeMirror browser editor featuring JavaScript/web syntax highlighting, auto-indentation, line numbering, and bracket matching.
- **Dynamic Room & Session Management:** Users can generate cryptographically unique UUID room tokens or join existing rooms with custom usernames.
- **Live Participant Awareness:** Real-time user presence indicators, instant join/leave event toasts, dynamic avatar indicators, and socket-level connection tracking.
- **Decoupled Cloud Architecture:** Frontend hosted on Vercel's global CDN, with the persistent WebSocket state engine deployed on Render for continuous connection longevity.

---

## 🛠️ Architecture & Tech Stack

### Frontend (`src/`)
- **Library:** React.js, React Router DOM
- **Editor Engine:** CodeMirror (`codemirror`), `react-codemirror2`
- **WebSocket Client:** `socket.io-client`
- **Notifications:** `react-hot-toast`
- **Utility:** `uuid` for unique room creation
- **Deployment:** Vercel

### Backend (`server.js`)
- **Server:** Node.js, Express.js
- **Real-Time Engine:** Socket.IO Server (`socket.io`)
- **State Management:** In-memory socket-to-room mapping & user connection pools
- **Deployment:** Render (Persistent Web Service with native WebSocket support)

---

## 📁 Repository Structure
```
groov-editor/
├── public/
│   ├── index.html              # Custom metadata, fonts & responsive viewport
│   └── code-sync.png           # Platform branding
├── src/
│   ├── components/
│   │   ├── Client.js           # Connected participant avatar & username badge
│   │   └── Editor.js           # CodeMirror instance & Socket.IO event bindings
│   ├── pages/
│   │   ├── Home.js             # Room creation & joining portal
│   │   └── EditorPage.js       # Main workspace layout with participant sidebar
│   ├── Actions.js              # Centralized Socket event action definitions
│   ├── socket.js               # Client socket factory with transport fallbacks
│   ├── App.js                  # Routing & toaster provider
│   └── index.js
├── server.js                   # Node.js + Express + Socket.IO server
├── render.yaml                 # 1-Click Render cloud blueprint
└── package.json
```

---

## ⚙️ Environment Variables

### Frontend (`.env`)
```env
REACT_APP_BACKEND_URL="https://groov-editor-server.onrender.com"
```

---

## 🚀 Local Development

1. **Clone the repository:**
   ```bash
   git clone https://github.com/groov33/groov-editor.git
   cd groov-editor
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Run the backend server:**
   ```bash
   npm run server:dev
   ```

4. **In a separate terminal, start the React frontend:**
   ```bash
   npm start
   ```

---

## 👤 Author
**Ayush Pandey**  
*National Institute of Technology, Tiruchirappalli (NIT Trichy)*  
* **Email:** [realayush44@gmail.com](mailto:realayush44@gmail.com)  
* **GitHub:** [@groov33](https://github.com/groov33)  
* **LinkedIn:** [Ayush Pandey](https://linkedin.com)
