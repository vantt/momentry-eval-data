---
id: 2026-11-02-hook-chan-lenh-co-chu-build-40f9
code: M-3SXH
aliases: [M-3SXH]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L75", "claude:c4caee3c#L204", "claude:c4caee3c#L612", "claude:c4caee3c#L791", "claude:c4caee3c#L3746"]
hook: "Chỉ vì chữ 'build', hook chặn lệnh và buộc đổi công cụ"
tension: cam_ma_van_lot
sides: ["Hook chặn lệnh để bảo vệ", "Chặn nhầm lệnh vô hại, làm chậm việc"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hook chặn lệnh có chữ 'build' hoặc đường dẫn node_modules, phải đổi công cụ

**Bối cảnh:** Một số hook của dự án chặn lệnh dựa trên từ khoá trong câu lệnh.
**Chuyện gì xảy ra:** Lệnh có chữ 'build' hoặc đường dẫn node_modules bị chặn nhiều lần, có lúc buộc agent đổi sang công cụ Edit để sửa file. Hook pre-push của upstream cũng chặn push cho đến khi phải đặt HUSKY=0 cho lệnh push. Những lần chặn này làm chậm đợt sửa nhưng không gây hỏng dữ liệu.
**Bài học:** Hook dựa trên từ khoá sinh ra chặn giả; thiết kế hook theo hành vi, và ghi cách bỏ qua hợp lệ vào tài liệu của dự án.
**Artefact:** Thông báo chặn của hook (đã bỏ đường dẫn).
