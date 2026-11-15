---
id: 2026-10-29-token-gateway-khong-duoc-in-ra-c455
code: M-651P
aliases: [M-651P]
date: 2026-10-29
repo: repo
status: raw
signals: [rang_buoc_thiet_ke]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:0faf0bb2#L823", "claude:0faf0bb2#L827", "claude:0faf0bb2#L891", "claude:0faf0bb2#L894", "claude:0faf0bb2#L895"]
hook: "Token không được in ra: script lấy thẳng từ tiến trình đang chạy"
tension: none
sides: []
strength: 0
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Token gateway không được in ra: script đọc từ môi trường của tiến trình đang chạy

**Bối cảnh:** Script tạo agent cần token của gateway nhưng không được để lộ trong log, file hay lệnh.
**Chuyện gì xảy ra:** Lần đầu script lỗi KeyError vì biến môi trường không có trong shell hiện tại. Mình tìm pid của gateway bằng ss rồi đọc /proc/<pid>/environ, token chỉ nằm trong bộ nhớ của script. Cách này được dùng lại cho các lệnh sau và được ghi vào runbook.
**Bài học:** Khi cần secret của một tiến trình đang chạy, đọc trực tiếp từ môi trường của tiến trình đó thay vì chép ra file.
**Artefact:** Đoạn lệnh, không kèm giá trị.
