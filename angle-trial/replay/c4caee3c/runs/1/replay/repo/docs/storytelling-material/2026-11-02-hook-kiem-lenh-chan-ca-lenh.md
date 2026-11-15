---
id: 2026-11-02-hook-kiem-lenh-chan-ca-lenh
date: 2026-11-02
repo: repo
status: raw
signals: [khác, ràng buộc định hình thiết kế]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L75", "claude:c4caee3c#L612", "claude:c4caee3c#L791", "claude:c4caee3c#L3746"]
hook: "Hook an toàn chặn cả lệnh vô hại chỉ vì có chữ build"
tension: giup_ma_hai
sides: ["Hook sinh ra để chặn lệnh nguy hiểm", "Chặn nhầm lệnh vô hại có chữ build hay node_modules, 4 lần"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hook kiểm lệnh chặn cả lệnh vô hại có từ build hay node_modules

**Bối cảnh:** Harness có hook quét từ khoá trong lệnh shell, nên một số lệnh hoàn toàn hợp lệ vẫn bị chặn.
**Chuyện gì xảy ra:** Bốn lần lệnh bị chặn vì chứa từ build, node_modules hoặc đường dẫn cần thêm vào file .ckignore. Agent phải chuyển sang công cụ Edit để sửa file, hoặc viết lại lệnh theo cách khác.
**Bài học:** Hook theo từ khoá dễ chặn nhầm; chuẩn bị sẵn danh sách ngoại lệ cho các lệnh build và test hợp lệ.
**Artefact:** Thông báo hook, đã che đường dẫn.
