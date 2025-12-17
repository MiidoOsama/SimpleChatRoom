# FastAPI WebSocket Chat Demo

A simple real-time chat application built with **FastAPI** and **WebSockets**. This project demonstrates how to establish WebSocket connections, manage multiple clients, and broadcast messages between them using FastAPI.

## 🚀 Features

* Real-time communication using WebSockets
* Multiple clients support (broadcast messages)
* Simple connection manager
* Basic HTML + Bootstrap frontend
* Unique client ID for each connection

## 🛠️ Tech Stack

* **Backend:** FastAPI
* **Frontend:** HTML, JavaScript, Bootstrap 5
* **Protocol:** WebSocket
* **Server:** Uvicorn

## 📁 Project Structure

```
.
├── main.py        # FastAPI application
└── README.md
```

## ▶️ How It Works

* When a user opens the webpage, a WebSocket connection is created.
* Each client gets a unique `client_id`.
* Messages sent by one client are:

  * Sent back to the same client (personal message)
  * Broadcasted to all connected clients
* When a client disconnects, all users are notified.

## ⚙️ Installation & Run

### 1. Create virtual environment (optional)

```bash
python -m venv venv
source venv/bin/activate  # Linux / Mac
venv\Scripts\activate     # Windows
```

### 2. Install dependencies

```bash
pip install fastapi uvicorn
```

### 3. Run the application

```bash
uvicorn main:app --reload
```

### 4. Open in browser

```
http://localhost:8000
```

Open the link in multiple tabs to test real-time chat.

## 🔌 WebSocket Endpoint

```
/ws/{client_id}
```

* Accepts WebSocket connections
* Handles sending and broadcasting messages

## 📸 Demo UI

* Input field to send messages
* Live message list
* Displays your unique client ID

## 📝 Notes

* This demo uses in-memory connections (not production-ready)
* No authentication included

##
