---
id: 2026-11-01-runtime-profile-offline-du-lenh-boc
date: 2026-11-01
repo: repo
status: raw
signals: ["2", "3"]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L2897", "claude:f0bf048d#L2908", "claude:f0bf048d#L2910", "claude:f0bf048d#L2929", "claude:f0bf048d#L2938", "claude:f0bf048d#L2948"]
hook: "2 runtime báo offline dù đã bọc lệnh: daemon chỉ nhìn lại khi profile bị sửa"
tension: cam_ma_van_lot
sides: ["Lệnh bọc đã có, tưởng runtime sẽ tự lên", "Daemon chỉ dò lại khi profile đổi nên vẫn offline"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Runtime profile offline dù lệnh bọc đã có: daemon chỉ dò lại khi profile đổi

**Bối cảnh:** Đổi tên profile trước khi cài lệnh bọc; daemon bỏ qua vì không tìm thấy lệnh.
**Chuyện gì xảy ra:** Hai runtime OpenAI ở hai workspace báo offline. Daemon chỉ dò lại profile khi profile bị sửa. Tắt rồi bật lại profile thì cả hai lên online trong vòng vài lần kiểm, tổng cộng 6 profile đã chạy.
**Bài học:** Daemon không tự dò lại khi lệnh xuất hiện sau; tạo lệnh bọc trước, đặt tên profile sau, hoặc kích hoạt lại profile.
**Artefact:** Bảng runtime online/offline trước và sau khi bật lại.
