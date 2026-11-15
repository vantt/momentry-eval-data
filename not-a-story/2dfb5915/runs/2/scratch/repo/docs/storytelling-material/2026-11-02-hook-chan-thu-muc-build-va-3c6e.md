---
id: 2026-11-02-hook-chan-thu-muc-build-va-3c6e
code: M-VZN1
aliases: [M-VZN1]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:2dfb5915#L506", "claude:2dfb5915#L1078", "claude:2dfb5915#L1460"]
hook: "Hook chặn cả build lẫn thư mục target, agent audit chỉ còn đoán từ mã"
tension: cam_ma_van_lot
sides: ["Hook chặn để an toàn, cấm build và đọc thư mục target", "Agent audit không chạy được binary nên phải suy từ mã nguồn thay vì kiểm chứng"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hook chặn thư mục build và lệnh sleep dài

**Bối cảnh:** Repo có hook scout-block và cơ chế ckignore chặn truy cập vào thư mục build, còn một hook khác chặn lệnh sleep nối dài.
**Chuyện gì xảy ra:** Hook chặn cả cargo build lẫn đọc thư mục target, nên agent audit không chạy được binary để kiểm chứng và phải suy từ mã nguồn. Một lệnh sleep 30 nối với lệnh khác bị chặn, hook yêu cầu dùng vòng until hoặc chạy nền.
**Bài học:** Hook bảo vệ có thể làm agent không kiểm chứng được thứ nó báo cáo. Cần ghi rõ trong báo cáo là kết quả suy từ mã, chưa chạy.
