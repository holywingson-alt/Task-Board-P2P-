# TracBoard — P2P Task Board

> A decentralized, peer-to-peer task board built on top of [Intercom](https://github.com/Trac-Systems/intercom) by Trac Systems.

---

<img width="1254" height="818" alt="image" src="https://github.com/user-attachments/assets/1a22fbf3-791a-4fb1-af1f-398365008678" />


## 📌 What is TracBoard?

**TracBoard** is a lightweight P2P task management board powered by the Intercom agent network. Users and agents can create, assign, update, and resolve tasks — all coordinated over Intercom sidechannels with state replicated on the Trac Network durable layer.

No central server. No database. Just agents talking to each other.

---

## ✨ Features

- ✅ Create and manage tasks in real-time via P2P sidechannels
- 🤝 Assign tasks to agents or peers on the Intercom network
- 🔄 Live task status updates: `TODO → IN PROGRESS → DONE`
- 🧠 Agent-compatible: accepts and processes task commands autonomously
- 📦 Fully static frontend (`index.html`) — zero dependencies, runs offline
- 🔐 Non-custodial — no login, no accounts, just your Trac identity

---

## 🚀 Live Demo

Open `index.html` in any browser — no server required.

The demo shows a fully functional kanban-style task board with:
- Drag-and-drop columns (TODO / IN PROGRESS / DONE)
- Add, edit, delete tasks
- Simulated P2P sync animation
- Agent command interface

---

## 🛠 How It Works

TracBoard uses Intercom sidechannels for lightweight agent-to-agent coordination:

1. A **Task Creator** agent posts a new task object over an Intercom sidechannel.
2. **Worker agents** listen, claim tasks, and update status via the replicated state layer.
3. The board UI subscribes to state changes and renders updates in real-time.
4. All state is persisted on the Trac Network durable layer — survives agent restarts.

```
[User/Agent] → Intercom Sidechannel → [Worker Agents]
                                           ↓
                                   Trac Replicated State
                                           ↓
                                    TracBoard UI Update
```

---

## 📂 Repo Structure

```
/
├── index.html       # Full demo app (self-contained, no dependencies)
├── SKILL.md         # Agent instructions for TracBoard
└── README.md        # This file
```

---

## 🧩 Fork Info

- **Forked from:** [Trac-Systems/intercom](https://github.com/Trac-Systems/intercom)
- **App type:** P2P Task Management Board
- **Stack:** Vanilla HTML/CSS/JS + Intercom agent layer

---

## 💰 Trac Address

> **TNK Payout Address:** `trac1q3gp0e0wr7uddlpl9adsqa9yzecwer7ly92utgzn7th799fms38sdjllzj`

*(Replace with your actual Trac address before submission)*

---

## 📜 License

MIT — fork freely, build boldly.
