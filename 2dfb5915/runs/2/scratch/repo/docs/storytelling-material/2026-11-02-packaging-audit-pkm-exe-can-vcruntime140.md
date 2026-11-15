---
id: 2026-11-02-packaging-audit-pkm-exe-can-vcruntime140
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, artefact]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1063", "claude:2dfb5915#L1078", "claude:2dfb5915#L1132"]
hook: "Agent tự sửa báo cáo audit của chính mình"
tension: khac
sides: ["báo cáo ghi action chưa kiểm", "thực tế đã dispatch thành công"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Packaging audit: pkm.exe cần vcruntime140.dll

**Bối cảnh:** Audit đóng gói theo skill, chỉ đọc không chạy.
**Chuyện gì xảy ra:** pkm.exe phụ thuộc vcruntime140.dll, nhiều máy Windows sạch không có, nên Claude Desktop có thể không chạy được. Nguyên nhân là không đặt crt-static. Audit chia lỗi thành ba chặn, chín quan trọng và tám nên có. Chính agent sửa báo cáo của mình: nó đã ghi các action v7 chưa kiểm, nhưng thực tế đã dispatch thành công.
**Bài học:** Kiểm phụ thuộc động của binary Windows, ví dụ bằng dumpbin, trước khi phát hành.
**Artefact:** Danh sách DLL import, không cần chụp.
