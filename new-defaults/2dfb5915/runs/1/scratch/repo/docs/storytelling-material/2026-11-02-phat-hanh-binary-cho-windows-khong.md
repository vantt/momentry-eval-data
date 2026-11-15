---
id: 2026-11-02-phat-hanh-binary-cho-windows-khong
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, artefact nhìn được]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L1072", "claude:2dfb5915#L1132", "claude:2dfb5915#L1237", "claude:2dfb5915#L1244"]
hook: "Thiếu một cờ build, binary Windows đòi người dùng cài thêm thư viện"
tension: nho_ma_to
sides: ["Thiếu một cờ crt-static trong cấu hình", "Máy Windows sạch không chạy được binary nếu thiếu vcruntime"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Phát hành binary cho Windows không cần vcruntime: một bước kiểm DLL trong CI

**Bối cảnh:** Audit đóng gói phát hiện binary pkm.exe phụ thuộc vcruntime140.dll, nhiều máy Windows sạch không có DLL đó, nên Claude Desktop không khởi động được.
**Chuyện gì xảy ra:** Gốc lỗi nhỏ: không có cờ crt-static trong cấu hình build. Sửa bằng .cargo/config.toml và một bước CI dùng dumpbin liệt kê DLL, fail nếu còn C runtime. Release dry run ra 7 file, sha256 đều khớp.
**Bài học:** Thêm một bước kiểm phụ thuộc DLL vào CI để lỗi đóng gói lộ sớm, thay vì chờ người dùng báo.
**Artefact:** Danh sách 7 file release và kết quả sha256; che tên tài khoản.
**Góc người ngoài:** cách làm phổ biến là Build thủ công trên máy dev, copy file lên release, không kiểm checksum hay phụ thuộc DLL; ở đây khác ở Gắn thêm bước CI cho từng nguy cơ đã biết (thiếu DLL, lệch checksum, tag không khớp version), và dùng workflow_dispatch để thử phát hành trước khi gắn tag thật. Người đọc muốn biết cách làm kiểm tra này trước khi người dùng gặp lỗi.
