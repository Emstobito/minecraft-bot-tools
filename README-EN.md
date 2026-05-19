# Minecraft Bot Manager

A desktop application for managing multiple Minecraft bots simultaneously, featuring a modern web-based UI running on Windows. Supports Minecraft versions from 1.8.9 to 1.21.11.

---

## Features

### Multi-Bot Management
- Each bot runs in its own **independent tab** — open unlimited bots in parallel
- **Grid view mode**: displays all bots as compact cards with a configurable column count
- Tab bar auto-scrolls when many tabs are open; left/right scroll buttons appear as needed

### Connection & Configuration
- Supports **Minecraft 1.8.9 → 1.21.11** (auto-detect or manual version selection)
- Per-bot **SOCKS4 / SOCKS5** proxy support
- **Auto Login**: automatically sends `/login` / `/register` commands when the server requests it
- **Auto Reconnect**: reconnects on disconnect with configurable delay and exponential backoff

### Bot Interface
Each bot has its own panel with two display modes:

**Standard tab mode:**
- `System Log` — full connection log, events, and errors
- `Chat` — server chat with a search bar
- `PM` — private messages with unread badge
- `Transactions` — `/pay`, `/baltop`, economy scoreboard with unread badge
- `Players` — online player list with ping, configurable column count
- `Inventory` — full inventory view (armor, offhand, main 9×3, hotbar)
- `Radar` — 2D entity radar (players, mobs, items, XP) with range 16/32/64/128/256 blocks

**Split 2×2 mode:**  
Toggle with the `⊞` button — splits the screen into 4 fixed panels:
- Top-left: System Log / Chat / PM / Transactions (tabbed)
- Top-right: Players
- Bottom-left: Inventory
- Bottom-right: Radar

### Bot Controls
- On-screen **D-pad** (WASD) + keyboard shortcuts (when the tab is active)
- **Attack** / **Use item**
- **AFK mode** — prevents idle kick using randomized anti-detection movement
- **Hotbar** — click to select slot
- **Inventory click** — left/right click, shift-click, drop item
- **Plugin GUI** — open and interact with server-side containers and chests

### Smart Command Bar
Quick-send bar with player name auto-complete:
```
/pay  /msg  /shards pay  /shards request  /baltop  /warp  /tp  /tpa  /kill  /cf  ...
```

### Entity Radar
- Realtime 2D canvas, updated every 3 seconds
- Categories: Player / Hostile / Passive / Neutral / Boss
- Heading-up mode and item/XP visibility toggle
- Detailed tooltip on hover

### Realtime Stats
Each bot's status bar displays:
- Server address, account name, ping
- Balance (`$`) and shards (`★`) — auto-updated
- Health ❤ and food 🍗 bars
- XYZ coordinates

---

## Tech Stack

| Component | Technology |
|---|---|
| Desktop shell | Electron 42 |
| Bot engine | mineflayer 4.37.1 |
| UI ↔ Server communication | Socket.io |
| UI | Vanilla JS + CSS Grid (no framework) |
| Proxy | SOCKS4/5 via `socks` library |

---

## System Requirements

- Windows 10/11 x64
- No Java or Minecraft client installation required

---

## Installation

### Using the installer (recommended)

Download `Minecraft Bot Manager Setup x.x.x.exe` from the `dist/` folder and run it.

---

## Bot Configuration (full schema)

```json
{
  "username": "Steve",
  "server": "play.example.com",
  "port": 25565,
  "version": "1.21.11",
  "autoLogin": {
    "enabled": true,
    "loginCommand": "/login YourPassword",
    "registerCommand": "/register YourPassword YourPassword",
    "triggerKeyword": "",
    "delay": 1000
  },
  "autoReconnect": {
    "enabled": true,
    "delay": 5000,
    "maxAttempts": 0,
    "exponentialBackoff": false
  },
  "afk": {
    "enabled": true
  },
  "proxy": {
    "enabled": false,
    "type": 5,
    "host": "127.0.0.1",
    "port": 1080,
    "username": "",
    "password": ""
  }
}
```

---

## License

Private — All rights reserved.
