---
id: 2026-11-03-thu-tu-tinh-trusted-hash-cua-d5ef
code: M-HQGB
aliases: [M-HQGB]
date: 2026-11-03
repo: repo
status: raw
signals: [dao_quyet_dinh]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L3106", "claude:ab9a1dd8#L3117", "claude:ab9a1dd8#L3121", "claude:ab9a1dd8#L3139", "claude:ab9a1dd8#L3149", "claude:ab9a1dd8#L3213", "claude:ab9a1dd8#L3239"]
hook: "Tự tính hash dễ sai, bật cờ bỏ duyệt vẫn không thấy hook"
tension: giup_ma_hai
sides: ["Dùng cờ bypass chính thức để hook chạy", "Probe vẫn không thấy hook gọi"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Thử tự tính trusted_hash của Codex rồi chuyển sang cờ bỏ duyệt

**Bối cảnh:** Mỗi hook của Codex cần một hash tin cậy, và việc duyệt hash nằm sau một bước thường không lộ ra.
**Chuyện gì xảy ra:** Agent định tự tái tạo cách tính hash từ mã nguồn, nhận ra dễ sai khi phải mô phỏng cách chuẩn hoá cấu hình, nên tìm cờ bypass_hook_trust chính thức. Probe chạy với cờ vẫn không thấy hook gọi. Nhiều khả năng phiên dừng trước bước hook, nhưng chưa chứng minh được.
**Bài học:** Đừng tự tái tạo một cơ chế tin cậy từ mã nguồn khi có cờ chính thức; và một probe không đủ điều kiện thì không kết luận được.
