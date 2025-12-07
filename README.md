# Haven — Privacy‑focused Real‑time Chat 💬🔒

[![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)]()
[![Made with Node.js](https://img.shields.io/badge/Node.js-%3E%3D14-339933.svg)]()
[![Socket.IO](https://img.shields.io/badge/Realtime-Socket.IO-010101.svg)]()

Haven is a lightweight, privacy-first one-on-one chat web application. It’s built with plain HTML/CSS/JavaScript on the frontend and Node.js + Express + Socket.IO on the backend. The app focuses on ephemeral, private conversations with a clean, responsive UI that works well on desktop and mobile.

Highlights
- 💬 Real-time messaging with Socket.IO
- 🔐 Private rooms (room code + password)
- ⌨️ Typing indicators and online status
- 😊 Emoji picker and auto-scrolling chat
- 🌗 Light/Dark theme toggle
- 📱 Mobile-friendly input handling (avoids keyboard overlap)
- 🕶️ Ephemeral chats — no persistent message storage by default

Table of Contents
- Features
- How it works
- Tech stack
- Quick start (local)
- Configuration
- Development notes
- Privacy & Security
- Contributing
- License
- Contact

Features
- 💨 Instant messaging using Socket.IO.
- 🔑 Private rooms protected by a room code and password.
- 👀 Presence indicators: see when your peer is online and typing.
- 😊 Emoji palette for quick expressive messaging.
- 🔁 Auto-scroll keeps the view at the latest message.
- 🌓 Theme switcher (light/dark).
- 📲 Viewport handling to keep input visible above the mobile keyboard.
- ❌ Exit confirmation to avoid accidental room leaving.
- 🗑️ Ephemeral by design — no default persistent storage.

How it works (user flow)
1. 📝 Login: Enter a username, room code, and password to create or join a room.
2. ↔️ Chat: Messages are exchanged in real time. Typing and online indicators show peer activity.
3. 😄 Emojis: Use the emoji button to insert emojis into messages.
4. 🎨 Theme: Toggle between light and dark UI themes.
5. 🚪 Exit: Leave the room with a confirmation prompt.

Technology stack
- Frontend: HTML, CSS, JavaScript (vanilla) — icons and small UI helpers use inline emojis.
- Backend: Node.js, Express, Socket.IO

Quick start (local)
Prerequisites
- Node.js (v14+ recommended)
- npm

Steps
1. Clone the repository:
   git clone https://github.com/TamimFiroz/Haven-App.git
2. Install backend dependencies:
   cd backend
   npm install
3. Start the backend server:
   node server.js
   (or use nodemon for development)
4. Open the frontend:
   - Open index.html in your browser, or
   - Serve the project with a static server (recommended for some browser APIs), e.g.:
     npx http-server . -c-1
   Then open the served URL in two separate browser windows/tabs to test one-on-one chat.

Configuration
- ⚙️ Server port and other settings can be defined in server.js or via environment variables.
- 🔒 If deploying publicly, use HTTPS and consider a reverse proxy (Nginx/Caddy) configuration.

Development notes
- 🧩 Backend exposes Socket.IO event handlers to manage rooms, presence, typing indicators, and message delivery.
- 🧭 Frontend is intentionally minimal for portability — consider migrating to a framework for larger features.
- ➕ To add file sharing or group chats, plan server-side storage, moderation, and privacy controls first.

Privacy & Security
- 🛡️ This app is designed for ephemeral chats — no persistent message store by default. If you add persistence, document retention policies clearly.
- 🔐 Use HTTPS in production to protect messages in transit.
- 🧹 Sanitize inputs and add rate limiting if you deploy publicly.

Contributing
Contributions, bug reports, and feature requests are welcome.
- Fork the repo
- Create a feature branch (git checkout -b feat/your-feature)
- Commit and push, then open a pull request describing your changes

License
- If you want MIT, add a LICENSE file with the MIT text. The badge above assumes MIT.

Contact
- Author: TamimFiroz
- Repo: https://github.com/TamimFiroz/Haven-App
- For questions or feedback, open an issue or PR in the repository.

Icons used
- 💬 Chat / main app
- 🔒 Privacy / security
- 📱 Mobile
- 😊 Emoji support
- 🌗 Theme toggle
- 🔁 Auto-scroll / realtime

Optional next improvements I can add for you
- Replace emoji icons with SVG icon images for a more polished README (logo, screenshots).
- Add live badges (CI, npm, GitHub release) once those services are configured.
- Add example environment variable names and values to server config.
