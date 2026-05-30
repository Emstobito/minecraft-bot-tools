# SharinTools — Hướng dẫn sử dụng

> Phần mềm quản lý bot Minecraft đa tài khoản, hỗ trợ vietmc.xyz và các server 1.21.x.

---

## Tải về

**[⬇ Download SharinTools (Google Drive)](https://drive.google.com/drive/folders/1DlZumNqEwBkXcFnuMlypuXnmiDSxHjyA)**

> Yêu cầu: Windows 10/11 64-bit. Không cần cài thêm bất kỳ phần mềm nào.

---

## Cài đặt

1. Tải file `SharinTools Setup x.x.x.exe` từ link trên.
2. Chạy file cài đặt → nhấn **Install** → chờ xong → **Finish**.
3. Mở **SharinTools** từ Desktop hoặc Start Menu.
4. Kích hoạt phần mềm theo hướng dẫn bên dưới trước khi dùng.

---

## Kích hoạt phần mềm

SharinTools sử dụng hệ thống kích hoạt 2 lớp gắn với thiết bị của bạn.

### Bước 1 — Lấy Device ID

Mở phần mềm → sao chép **Device ID** (chuỗi 32 ký tự hiển thị sẵn).

### Bước 2 — Liên hệ dev để nhận token

Gửi **Device ID** cho dev qua:

- **Discord:** `[tên Discord của bạn]`

Kèm theo gói bạn muốn mua (Standard / Pro / Elite). Dev sẽ cấp cho bạn **2 token**:

| Token | Mô tả |
|-------|-------|
| **License Token** | Kích hoạt vĩnh viễn, gắn với thiết bị |
| **Time Key Token** | Mở tính năng theo thời hạn (VD: 30 ngày) |

### Bước 3 — Nhập token vào phần mềm

1. Trong tab **License**, dán **License Token** vào ô *License*.
2. Dán **Time Key Token** vào ô *Time Key*.
3. Nhấn **Activate** → phần mềm sẵn sàng sử dụng.

> **Lưu ý:** Token gắn với Device ID của máy bạn. Không dùng được trên máy khác.  
> Khi Time Key hết hạn, liên hệ dev để gia hạn — không cần gửi lại Device ID.

---

## Các gói dịch vụ

| Tính năng | Standard | Pro | Elite |
|-----------|:--------:|:---:|:-----:|
| Số bot đồng thời | 3 | 6 | Không giới hạn |
| Chat & System log | ✅ | ✅ | ✅ |
| Auto Login / Reconnect | ✅ | ✅ | ✅ |
| AFK tự động | ✅ | ✅ | ✅ |
| Hỗ trợ Proxy | ✅ | ✅ | ✅ |
| Tab PM (tin nhắn riêng) | ❌ | ✅ | ✅ |
| Tab Giao dịch | ❌ | ✅ | ✅ |
| Inventory viewer | ❌ | ✅ | ✅ |
| Radar (danh sách người chơi gần) | ❌ | ✅ | ✅ |
| Grid view (xem nhiều bot cùng lúc) | ❌ | ✅ | ✅ |

---

## Tính năng chính

### Quản lý nhiều bot
- Mỗi bot chạy trong một **tab** riêng. Nhấn **+** để thêm bot mới.
- Xem tổng quan tất cả bot cùng lúc qua **Grid View** (Pro+).

### Auto Login
Tự động phát hiện thông báo đăng nhập từ server và gõ lệnh `/login` — không cần ngồi chờ.

### Auto Reconnect
Bot tự kết nối lại khi bị ngắt. Hỗ trợ:
- Delay tùy chỉnh (mặc định 5 giây)
- Số lần thử tối đa (0 = không giới hạn)
- Exponential backoff (tăng dần thời gian chờ)

### AFK tự động
Giữ bot luôn trực tuyến, tự động chống AFK-kick của server.

### Hỗ trợ Proxy
Kết nối qua **SOCKS4**, **SOCKS5**, hoặc **HTTP** proxy — mỗi bot có thể dùng proxy riêng.

### Theo dõi Chat & Giao dịch
- Tab **Chat**: toàn bộ chat server, có thanh tìm kiếm.
- Tab **PM**: lọc riêng tin nhắn gửi cho bot.
- Tab **Giao dịch** (Pro+): lọc và lưu lịch sử giao dịch.

### Inventory Viewer (Pro+)
Xem inventory của bot theo thời gian thực — thanh hot-bar, ba lô, giáp đang mặc.

### Radar (Pro+)
Danh sách người chơi xung quanh bot kèm khoảng cách.

### Gửi lệnh & Chat
Gõ lệnh chat hoặc command trực tiếp từ giao diện, không cần vào game.

---

## Câu hỏi thường gặp

**Q: Phần mềm có bị phát hiện không?**  
A: SharinTools mô phỏng hành vi client thật ở mức protocol. Tuy nhiên không có công cụ nào đảm bảo 100% — dùng trên tài khoản phụ để an toàn.

**Q: Đổi máy tính thì sao?**  
A: License gắn với máy. Liên hệ dev để chuyển license sang Device ID mới (giới hạn số lần chuyển).

**Q: Time Key hết hạn mà chưa kịp gia hạn thì bot có bị xóa không?**  
A: Không. Cài đặt bot và license vẫn còn nguyên. Chỉ các tính năng theo gói bị khóa cho đến khi gia hạn.

**Q: Hỗ trợ phiên bản Minecraft nào?**  
A: Hiện tại hỗ trợ **1.21.x** (bao gồm 1.21.11).
