---
id: 2026-11-02-prd-ghi-viet-lai-bang-rust-40f9
code: M-BENG
aliases: [M-BENG]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
signal_note: "Hai việc khác nhau trong kế hoạch dùng cùng một cách diễn đạt dễ bị đọc nhầm, nên chủ dự án phải hỏi lại nhiều lần."
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L2226", "claude:c4caee3c#L2302", "claude:c4caee3c#L2368", "claude:c4caee3c#L2394", "claude:c4caee3c#L2430", "claude:c4caee3c#L2450", "claude:c4caee3c#L2458", "claude:c4caee3c#L2466"]
hook: "PRD ghi 'viết lại bằng Rust', ai cũng tưởng là bỏ script Python"
tension: tuong_ma_hoa_ra
sides: ["Tưởng L15 là bỏ script Python", "Thực ra là hai việc hoàn toàn khác"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# PRD ghi 'viết lại bằng Rust' và 'chạy script Python' dễ đọc nhầm

**Bối cảnh:** Kế hoạch có nhiều việc thuộc repo dự án chứ không thuộc fork, và một mục N13 nói về Rust.
**Chuyện gì xảy ra:** Chủ dự án hỏi L15 có phải là các script Python bị bỏ không. Agent trả lời đó là hai việc khác nhau: L15 là viết lại toàn bộ OHS bằng Rust, còn script Python là V16 thuộc repo dự án. PRD được sửa hai lần cho rõ. Các mục L13 và L22 cũng được chuyển sang repo dự án sau nhiều câu hỏi.
**Bài học:** Đặt tên việc theo đối tượng cụ thể, và ghi rõ việc nào thuộc repo nào ngay từ đầu.
