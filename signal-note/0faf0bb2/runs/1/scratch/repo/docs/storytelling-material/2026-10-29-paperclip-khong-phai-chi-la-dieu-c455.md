---
id: 2026-10-29-paperclip-khong-phai-chi-la-dieu-c455
code: M-7GD0
aliases: [M-7GD0]
date: 2026-10-29
repo: repo
status: raw
signals: [dao_quyet_dinh, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:0faf0bb2#L1515", "claude:0faf0bb2#L1523", "claude:0faf0bb2#L1529", "claude:0faf0bb2#L1533", "claude:0faf0bb2#L1548", "claude:0faf0bb2#L1551", "claude:0faf0bb2#L1574", "claude:0faf0bb2#L1576"]
hook: "Mình gọi Paperclip là 'chỉ điều phối', nhưng nó có cả runtime Rust"
tension: tuong_ma_hoa_ra
sides: ["Tưởng Paperclip chỉ là lớp điều phối", "Nó kèm Native Runner Rust và giấu adapter OpenClaw"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Paperclip không phải chỉ là điều phối: có runtime riêng và UI giấu adapter OpenClaw

**Bối cảnh:** Khi tạo agent trên UI, chủ không thấy lựa chọn OpenClaw và nhận xét Paperclip giống một runtime hơn là một giao diện.
**Chuyện gì xảy ra:** Trong adapter-display-registry, openclaw_gateway được gắn comingSoon và hideFromVisualSelection, còn capabilities của nó đều là false. Paperclip còn kèm một Native Runner viết bằng Rust để chạy các CLI agent như Claude Code và Codex. Mình trước đó mô tả Paperclip là 'chỉ điều phối', và câu đó bị sửa.
**Bài học:** 'Chỉ là lớp điều phối' là giả định phải kiểm trong code; cờ ẩn trong UI là tín hiệu về hướng sản phẩm.
**Artefact:** Đoạn cấu hình adapter đã rút gọn, không kèm đường dẫn nội bộ.
