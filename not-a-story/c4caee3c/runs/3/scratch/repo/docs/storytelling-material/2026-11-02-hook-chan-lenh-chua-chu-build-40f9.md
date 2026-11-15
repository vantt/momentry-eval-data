---
id: 2026-11-02-hook-chan-lenh-chua-chu-build-40f9
code: M-1HJ8
aliases: [M-1HJ8]
date: 2026-11-02
repo: repo
status: raw
signals: [rang_buoc_thiet_ke, khac]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L75", "claude:c4caee3c#L612", "claude:c4caee3c#L791", "claude:c4caee3c#L3746"]
hook: "Hook chặn chữ build, bốn lần lệnh của agent bị từ chối"
tension: cam_ma_van_lot
sides: ["Hook chặn lệnh chứa build và node_modules", "Agent đổi sang công cụ Edit để làm được việc"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hook chặn lệnh chứa chữ build và node_modules, agent phải đổi cách làm

**Bối cảnh:** Hook bảo vệ của dự án chặn một số từ trong lệnh shell, nên các agent gặp chặn lặp đi lặp lại.
**Chuyện gì xảy ra:** Ít nhất bốn lần lệnh bị chặn: hai lần vì có node_modules, một lần vì có chữ build trong lệnh kiểm tra, một lần vì có chữ build trong đường dẫn sửa file. Agent phải chuyển sang công cụ Edit hoặc đổi cách gọi lệnh, thay vì xin mở quyền cho từng từ.
**Bài học:** Hook an toàn nên nói rõ từ nào bị chặn và cách làm hợp lệ, nếu không mọi agent sẽ tự tìm đường vòng.
**Artefact:** Dòng thông báo của hook, không kèm đường dẫn.
