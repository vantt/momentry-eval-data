---
id: 2026-11-02-may-windows-tim-2-lech-cli
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, ràng buộc định hình thiết kế]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1822", "claude:2dfb5915#L1873", "claude:2dfb5915#L3233", "claude:2dfb5915#L3969"]
hook: "CI xanh ba hệ điều hành, nhưng máy Windows thật vẫn tìm ra 2 lệch"
tension: cam_ma_van_lot
sides: ["CI xanh, golden không đổi", "Vault thật trên Windows lộ 2 lệch"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Máy Windows tìm 2 lệch CLI mà CI không thấy: đường dẫn escape trong JSON

**Bối cảnh:** Vault riêng của user không đưa lên CI được, nên CI chỉ so khớp trên vault mẫu.
**Chuyện gì xảy ra:** Máy Windows chạy bộ so khớp trên vault thật và thấy 2 lệch ở CLI: Scrub không che dạng đường dẫn có backslash escape trong JSON. Sửa để che cả hai dạng, dài nhất trước. Trên Linux hai dạng giống nhau nên golden không đổi. Lệch này chỉ lộ trên vault thật.
**Bài học:** Giữ một bộ kiểm chạy trên dữ liệu thật ở máy người dùng và tách phần che dữ liệu ra để kiểm riêng.
**Artefact:** Bảng 2 lệch trước và sau sửa, không có tên note.
