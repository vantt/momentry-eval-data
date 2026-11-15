---
id: 2026-11-02-may-windows-thu-ban-rc-ba-3c6e
code: M-N3N5
aliases: [M-N3N5]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L3242", "claude:2dfb5915#L3275"]
hook: "Cờ -I để an toàn lại làm script không thấy PyYAML của người dùng"
tension: giup_ma_hai
sides: ["Cờ -I cô lập Python cho an toàn", "Nó cũng ẩn luôn thư viện cài bằng pip --user"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Máy Windows thử bản rc: ba lỗi từ môi trường thật, trong đó -I ẩn luôn thư viện cài theo user

**Bối cảnh:** Một agent chạy trên máy Windows thật, không có Python trong PATH, thử cài bản rc.1 và chạy bộ so khớp.
**Chuyện gì xảy ra:** Ba lỗi: bộ che đường dẫn không che dạng backslash trong JSON nên lộ đường dẫn; in tiếng Việt qua pipe với cp1252 làm sập script; probe chạy python -I nên không thấy PyYAML cài bằng pip --user. Fix đổi sang -E -P: vẫn bỏ biến PYTHON* và không nạp code từ vault, nhưng vẫn thấy site của user.
**Bài học:** -I không chỉ là 'an toàn' mà còn tắt user site; khi cần cô lập mà vẫn dùng thư viện người dùng, hãy tách từng cờ thay vì dùng cờ gộp.
**Artefact:** Bảng ba lỗi và cách sửa. Không đưa đường dẫn Windows thật.
