---
id: 2026-11-02-chia-plan-thanh-cac-dot-wave
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:2dfb5915#L62", "claude:2dfb5915#L120", "claude:2dfb5915#L121", "claude:2dfb5915#L151", "claude:2dfb5915#L212", "claude:2dfb5915#L285", "claude:2dfb5915#L314", "claude:2dfb5915#L342", "claude:2dfb5915#L403", "claude:2dfb5915#L693", "claude:2dfb5915#L844"]
hook: "7 agent chạy song song trong 7 worktree, lead tự merge và test từng nhánh"
tension: none
sides: []
strength: 0
stakes: 2
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chia plan thành các đợt (wave): làm phase nền một mình, rồi chạy 7 phase độc lập song song, mỗi phase một agent trong worktree riêng. Lead tự merge từng nhánh, giải conflict, chạy lại fmt/clippy/test/parity sau mỗi merge rồi mới push.

**Chuyện gì xảy ra:** Chia plan thành các đợt (wave): làm phase nền một mình, rồi chạy 7 phase độc lập song song, mỗi phase một agent trong worktree riêng. Lead tự merge từng nhánh, giải conflict, chạy lại fmt/clippy/test/parity sau mỗi merge rồi mới push.
**Góc người ngoài:** cách làm phổ biến là Dùng một agent AI chạy tuần tự, hoặc mở nhiều cửa sổ chat rồi tự ghép tay. Hiếm ai điều phối nhiều agent có nhánh riêng; ở đây khác ở Làm được 17 phase trong thời gian ngắn mà main luôn xanh. Người đọc sẽ hỏi 'agent nào làm gì, ghép thế nào không vỡ'. Câu trả lời là phase có phụ thuộc rõ trong plan, mỗi agent một nhánh, lead là người duy nhất ghi vào main.
