# Smart Classroom Platform
 
Full-stack online classroom platform for virtual learning, assignments, and student–teacher collaboration. Built around real-time video sessions, role-based dashboards, and webcam-based attendance tracking.
 
## ✨ Features
 
- **Real-time virtual classrooms** — WebRTC video/audio sessions with Socket.io signaling for live classes.
- **Role-based dashboards** — separate views and permissions for **students**, **teachers**, and **admins**.
- **Face-recognition attendance** — webcam-based face capture and matching for automatic student check-in during sessions.
- **Authentication & security** — JWT-based auth with protected routes and role guards.
- **Live session management** — join/leave handling, participant tiles, camera & mic toggles.
- **Assignments & collaboration** — space for teachers to post assignments and manage class activity.
- **Announcements** — scoped announcements per class/session.
## 🛠️ Tech Stack
 
**Frontend**
- React + Vite
- Zustand (state management)
- face-api.js (face detection & recognition)
**Backend**
- Node.js + Express
- Socket.io (real-time communication / signaling)
- WebRTC (peer-to-peer video/audio)
- JWT (authentication)
## 📁 Project Structure
 
```
smart-classroom-platform/
├── client/                 # React + Vite frontend
│   ├── src/
│   │   ├── components/     # UI components (e.g. FaceCapture.jsx)
│   │   ├── store/          # Zustand stores
│   │   ├── pages/          # Route-level views (student/teacher/admin)
│   │   └── ...
│   └── package.json
├── server/                 # Node.js + Express backend
│   ├── routes/
│   ├── controllers/
│   ├── sockets/            # Socket.io / WebRTC signaling logic
│   ├── models/
│   └── package.json
└── README.md
```
 
> Adjust the tree above to match the actual folder layout once the repo contents are pushed.
 
## 🚀 Getting Started
 
### Prerequisites
- Node.js (v18+ recommended)
- npm or yarn
- A webcam-enabled browser (for attendance/video features)
### Installation
 
```bash
# Clone the repository
git clone https://github.com/jubayedahamed20-boop/smart-classroom-platform.git
cd smart-classroom-platform
 
# Install server dependencies
cd server
npm install
 
# Install client dependencies
cd ../client
npm install
```
 
### Environment Variables
 
Create a `.env` file in the `server/` directory:
 
```
PORT=5000
JWT_SECRET=your_jwt_secret
MONGODB_URI=your_database_connection_string
CLIENT_URL=http://localhost:5173
```
 
### Running the App
 
```bash
# Start the backend (from /server)
npm run dev
 
# Start the frontend (from /client)
npm run dev
```
 
The client will run on `http://localhost:5173` and the server on `http://localhost:5000` by default.
 
## 👥 Roles
 
| Role    | Capabilities                                                             |
|---------|---------------------------------------------------------------------------|
| Student | Join live classes, get marked present via face capture, view assignments |
| Teacher | Host sessions, manage attendance, post announcements/assignments         |
| Admin   | Manage users, oversee classes, system-wide controls                      |
 
## 🗺️ Roadmap
 
- [ ] Fix ghost/duplicate participant tiles on rejoin
- [ ] Exempt teachers from attendance check-in flow
- [ ] Improve video call reliability
- [ ] Expand assignment submission & grading features
## 🤝 Contributing
 
Contributions, issues, and feature requests are welcome. Feel free to open an issue or submit a pull request.
 

