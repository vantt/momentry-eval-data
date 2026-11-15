---
id: 2026-10-29-truoc-khi-chep-skill-hay-chay
date: 2026-10-29
repo: repo
status: raw
signals: []
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:0faf0bb2#L795", "claude:0faf0bb2#L807", "claude:0faf0bb2#L1268", "claude:0faf0bb2#L1269", "claude:0faf0bb2#L1270", "claude:0faf0bb2#L2812", "claude:0faf0bb2#L2815", "claude:0faf0bb2#L2825", "claude:0faf0bb2#L2826"]
hook: "Đọc và grep gói bên thứ ba trước khi chép vào workspace agent"
tension: none
sides: []
strength: 1
stakes: 0
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Trước khi chép skill hay chạy script từ gói của bên thứ ba vào workspace của agent, đọc nội dung và grep các mẫu đáng ngờ (curl, rm -rf, ssh, đẩy secret ra ngoài); tắt telemetry ngay khi cài; kiểm checksum khi tải binary

**Chuyện gì xảy ra:** Trước khi chép skill hay chạy script từ gói của bên thứ ba vào workspace của agent, đọc nội dung và grep các mẫu đáng ngờ (curl, rm -rf, ssh, đẩy secret ra ngoài); tắt telemetry ngay khi cài; kiểm checksum khi tải binary
**Góc người ngoài:** cách làm phổ biến là npx hoặc curl | sh rồi dùng luôn, telemetry để mặc định, ít ai kiểm checksum release; ở đây khác ở Gói chạy cùng quyền user và agent sẽ đọc skill đó như chỉ dẫn, nên thêm vài giây kiểm tra là đáng. Người đọc muốn danh sách kiểm tra tối thiểu khi thử công cụ agent mới.
