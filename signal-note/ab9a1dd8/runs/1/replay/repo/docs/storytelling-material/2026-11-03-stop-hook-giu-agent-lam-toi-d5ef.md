---
id: 2026-11-03-stop-hook-giu-agent-lam-toi-d5ef
code: M-E6Z7
aliases: [M-E6Z7]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L664", "claude:ab9a1dd8#L2233", "claude:ab9a1dd8#L2948", "claude:ab9a1dd8#L3047"]
hook: "Agent tưởng xong rồi, hook kéo về ba lần: 43/45 việc"
tension: tuong_ma_hoa_ra
sides: ["Agent nghĩ plan đã xong", "Hook đếm còn 43/45 và release chưa cắt"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Stop hook giữ agent làm tới khi plan đủ 45/45 và release xong: ba lần bị kéo về

**Bối cảnh:** Goal đặt cho agent là chạy /ak-cook --auto tới khi plan hoàn tất tốt đẹp; Stop hook chặn dừng cho tới khi điều kiện đúng.
**Chuyện gì xảy ra:** Ba lần hook trả feedback: plan còn 43/45 việc (hai việc cần push), plan 45/45 nhưng v0.1.0 chưa cắt, và Windows chưa đo hook thật. Mỗi lần agent làm thêm việc: push, cắt release, tạo workflow probe.
**Bài học:** Điều kiện dừng nên ghi rõ từng mục ra ngoài (push, release, đo thật) để khỏi phải hỏi lại; tốt đẹp không đo được.
**Artefact:** Ba feedback của Stop hook (đã tóm tắt).
