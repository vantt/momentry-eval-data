---
id: 2026-10-29-lenh-onboard-yes-khong-bao-gio
date: 2026-10-29
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L768", "claude:0faf0bb2#L779", "claude:0faf0bb2#L809"]
hook: "Lệnh onboard --yes không bao giờ kết thúc vì tự bật server"
tension: giup_ma_hai
sides: ["thêm cờ --yes để chạy khỏi cần hỏi", "lệnh tự khởi động server nên treo mãi không thoát"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Lệnh onboard --yes không bao giờ kết thúc vì tự khởi động server

**Bối cảnh:** Cài Paperclip bằng lệnh onboard với --yes và không cài service. Lệnh báo timeout 600 giây và chuyển sang chạy nền.
**Chuyện gì xảy ra:** Với cờ --yes, onboard tự khởi động server ngay nên không thoát. Mình kiểm tra port 3100 và thấy server đã lên. Telemetry được tắt bằng cả biến môi trường và file cấu hình.
**Bài học:** Đọc kỹ cờ tự động của công cụ: --yes có thể bao gồm bước chạy dịch vụ dài hạn.
**Artefact:** Không cần chụp.
