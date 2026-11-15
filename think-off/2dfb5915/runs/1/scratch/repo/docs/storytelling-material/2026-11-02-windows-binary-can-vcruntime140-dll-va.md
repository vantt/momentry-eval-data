---
id: 2026-11-02-windows-binary-can-vcruntime140-dll-va
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, ràng buộc định hình thiết kế]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1078", "claude:2dfb5915#L1237", "claude:2dfb5915#L1245"]
hook: "Máy Windows sạch thiếu một DLL, Claude Desktop không chạy server"
tension: nho_ma_to
sides: ["một file vcruntime140.dll bị thiếu", "server không chạy được trong Claude Desktop"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Windows: binary cần vcruntime140.dll, và tiếng Việt hỏng khi cài qua irm

**Bối cảnh:** Bản cài đầu tiên cho Windows. Audit đóng gói tìm ra 3 lỗi chặn.
**Chuyện gì xảy ra:** pkm.exe phụ thuộc vcruntime140.dll, nhiều máy Windows sạch không có DLL này, nên Claude Desktop không chạy được server. Đã build với CRT tĩnh và thêm bước CI kiểm tra không còn phụ thuộc DLL. PowerShell 5.1 đọc script qua irm làm hỏng dấu tiếng Việt, nên thông báo cài đặt chuyển sang tiếng Anh chỉ dùng ASCII.
**Bài học:** Thử bản cài trên máy sạch sớm. Kiểm DLL phụ thuộc trong CI. Script cài chạy qua pipe trên Windows PowerShell 5.1 chỉ nên có ASCII.
**Artefact:** Ảnh thông báo cài bị lỗi dấu, che đường dẫn người dùng.
