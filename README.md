# Minecraft Bot Manager

Ứng dụng desktop quản lý nhiều Minecraft bot cùng lúc, giao diện web hiện đại chạy trên Window. Hỗ trợ đầy đủ các phiên bản Minecraft từ 1.8.9 đến 1.21.11.

---

## Tính năng

### Quản lý đa bot
- Mỗi bot chạy trong một **tab độc lập**, có thể mở song song không giới hạn số lượng
- **Chế độ grid view**: hiển thị tất cả bot dưới dạng thẻ thu gọn, tuỳ chỉnh số cột
- Tab bar tự động scroll khi nhiều tab; nút cuộn trái/phải xuất hiện khi cần

### Kết nối & Cấu hình
- Hỗ trợ **Minecraft 1.8.9 → 1.21.11** (auto-detect hoặc chỉ định thủ công)
- Hỗ trợ proxy **SOCKS4 / SOCKS5** per-bot
- **Auto Login**: tự động gửi lệnh `/login` / `/register` khi server yêu cầu
- **Auto Reconnect**: kết nối lại khi bị ngắt, có thể cấu hình delay và exponential backoff

### Giao diện bot
Mỗi bot có panel riêng với hai chế độ hiển thị:

**Chế độ tab thông thường:**
- `System Log` — toàn bộ log kết nối, event, lỗi
- `Chat` — chat server (có thanh tìm kiếm)
- `PM` — tin nhắn riêng (có badge unread)
- `Giao dịch` — log /pay, /baltop, scoreboard kinh tế (có badge unread)
- `Players` — danh sách người chơi online với ping, tuỳ chỉnh số cột
- `Inventory` — hiển thị inventory đầy đủ (armor, offhand, main 9×3, hotbar)
- `Radar` — radar thực thể 2D (player, mob, item, XP) với range 16/32/64/128/256 block

**Chế độ split 2×2:**  
Bật bằng nút `⊞` — chia màn hình thành 4 ô cố định:
- Trên trái: System Log / Chat / PM / Giao dịch (tab)
- Trên phải: Players
- Dưới trái: Inventory
- Dưới phải: Radar

### Điều khiển bot
- **D-pad** WASD trên giao diện + phím bàn phím (khi tab đang active)
- **Attack** / **Use item**
- **AFK mode** — chống idle kick với chuyển động ngẫu nhiên anti-detection
- **Hotbar** — click để chọn slot
- **Inventory click** — click trái/phải, shift-click, drop item
- **Plugin GUI** — mở và tương tác với container/chest của server

### Smart Command
Thanh lệnh nhanh tích hợp auto-complete tên người chơi:
```
/pay  /msg  /shards pay  /shards request  /baltop  /warp  /tp  /tpa  /kill  /cf  ...
```

### Radar thực thể
- Vẽ canvas 2D realtime, cập nhật mỗi 3 giây
- Phân loại: Player / Hostile / Passive / Neutral / Boss
- Hỗ trợ chế độ "hướng lên" (heading-up) và hiện items/XP
- Tooltip chi tiết khi hover

### Thống kê realtime
Thanh trạng thái mỗi bot hiển thị:
- Server, tên tài khoản, ping
- Số dư tiền (`$`) và shards (`★`) — tự động cập nhật
- Thanh máu ❤ và no đói 🍗
- Toạ độ XYZ

---

## Công nghệ

| Thành phần | Công nghệ |
|---|---|
| Desktop shell | Bot engine |
| Giao tiếp UI ↔ Server | Socket.io |
| Proxy | SOCKS4/5 qua thư viện `socks` |

---

## Yêu cầu hệ thống

- Windows 10/11 x64
- Không cần cài Java hay Minecraft client

---

## Cài đặt

### Dùng installer (khuyến nghị)

Tải file `Minecraft Bot Manager Setup x.x.x.exe` từ thư mục `dist/` và chạy.


---

## Debug & Tools


---

## Cấu hình bot (đầy đủ)

```json
{
  "username": "Steve",
  "server": "play.example.com",
  "port": 25565,
  "version": "1.21.11",
  "autoLogin": {
    "enabled": true,
    "loginCommand": "/login MatKhau",
    "registerCommand": "/register MatKhau MatKhau",
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
