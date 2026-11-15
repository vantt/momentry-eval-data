---
id: 2026-11-01-goi-api-cap-nhat-agent-405-f60d
code: M-YP03
aliases: [M-YP03]
date: 2026-11-01
repo: repo
status: raw
signals: [nguyên nhân gốc nhỏ]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L2440", "claude:f0bf048d#L2445", "claude:f0bf048d#L2454", "claude:f0bf048d#L2457"]
hook: "PATCH báo 405, đọc router mới biết phải dùng PUT"
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

# Gọi API cập nhật agent: 405 vì dùng sai method, PUT mới cập nhật được

**Bối cảnh:** Chuyển 12 agent sang runtime mới bằng script gọi API.
**Chuyện gì xảy ra:** PATCH trả 405. Đọc router thấy đăng ký PUT cho cập nhật từng phần. Chạy lại với PUT, cả hai agent thử trả 200.
**Bài học:** Đọc router để biết method, đừng đoán từ quy ước REST.
**Artefact:** Hai dòng kết quả 405 rồi 200 (che id).
