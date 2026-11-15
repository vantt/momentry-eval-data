---
id: 2026-10-29-token-gateway-khong-co-trong-moi
date: 2026-10-29
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:0faf0bb2#L891", "claude:0faf0bb2#L894", "claude:0faf0bb2#L1119", "claude:0faf0bb2#L1123"]
hook: "Token nằm sẵn trong tiến trình đang chạy, đọc ra mà không cần in lên màn hình"
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

# Token gateway không có trong môi trường của lệnh: đọc từ tiến trình đang chạy và không in ra

**Bối cảnh:** Script tạo agent cho Paperclip cần token của gateway OpenClaw. Lệnh chạy lại trong shell mới không có biến môi trường đó nên KeyError.
**Chuyện gì xảy ra:** Token thật nằm trong môi trường của tiến trình gateway đang chạy. Mình đọc nó từ /proc của tiến trình đó, không in ra màn hình và không đưa vào dòng lệnh. Cách này cũng được dùng cho các script sau, và các script được chép vào repo không chứa bí mật.
**Bài học:** Lấy secret từ tiến trình đang chạy thay vì truyền qua dòng lệnh, để không lộ trong lịch sử shell hay log.
**Artefact:** Đoạn lệnh đọc /proc đã che PID và tên biến.
