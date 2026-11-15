---
id: 2026-10-29-lenh-tao-agent-ghi-de-openclaw-c455
code: M-1D12
aliases: [M-1D12]
date: 2026-10-29
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L2922", "claude:0faf0bb2#L2923"]
hook: "Một lệnh tạo agent âm thầm ghi đè openclaw.json; backup có nhờ bước trước"
tension: cam_ma_van_lot
sides: ["Chỉ là lệnh tạo agent", "Nó ghi đè cả cấu hình mà không cảnh báo"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Lệnh tạo agent ghi đè openclaw.json, chỉ có backup nhờ bước trước đó

**Bối cảnh:** Tạo agent OpenClaw mới bằng CLI để tách agent cho thử nghiệm Multica.
**Chuyện gì xảy ra:** Lệnh báo 'Config overwrite' kèm hash đổi từ bản cũ sang bản mới. Trước đó, agent đã copy openclaw.json sang thư mục spike, nên có thể khôi phục. CLI không cảnh báo trước khi ghi.
**Bài học:** Sao lưu file cấu hình trước khi gọi CLI có khả năng ghi lại nó.
**Artefact:** Dòng 'Config overwrite' kèm hash. Đã che đường dẫn.
