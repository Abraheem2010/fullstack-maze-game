# 🧩 Maze Game — Full-Stack Web App

A full-stack maze game with 3 stages and a Hall of Fame leaderboard.  
Each stage measures the player's completion time, sends the result to the backend,  
and the server stores only the best (fastest) record per stage.

## What it demonstrates
- A REST API (Express) with input validation and a SQLite-backed leaderboard
- Server-side "keep only the best time per stage" logic
- A React single-page client: multi-stage game flow + leaderboard view
- Full-stack wiring — the React build is served by the same Express server

## 🛠️ Tech Stack
- **Frontend:** React
- **Backend:** Node.js + Express
- **Database:** SQLite

## 📁 Project Structure
```
maze-game/
├── client/         # React frontend
│   └── src/
│       ├── stages/ # Maze1, Maze2, Maze3
│       └── App.js
├── server/         # Express backend
│   ├── server.js
│   └── db.js       # SQLite connection — auto-creates maze_records.db on first run
```

## ⚙️ Installation & Running Locally

### Backend
```bash
cd server
npm install
node server.js
```

### Frontend
```bash
cd client
npm install
npm start
```

## 📡 API Endpoints
| Method | Route | Description |
|--------|-------|-------------|
| POST | /api/score | Submit a new score |
| GET | /api/records | Get all best records |

## 🎮 How to Play
1. Enter your name on the home screen
2. Complete all 3 maze stages as fast as possible
3. Your best time is saved to the leaderboard
4. Check the Hall of Fame to see top records!

