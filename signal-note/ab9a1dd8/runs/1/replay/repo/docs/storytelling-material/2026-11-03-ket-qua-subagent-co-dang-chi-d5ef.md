---
id: 2026-11-03-ket-qua-subagent-co-dang-chi-d5ef
code: M-M7M4
aliases: [M-M7M4]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
signal_note: Đầu ra công cụ chứa dạng chỉ dẫn; ranh giới giữa dữ liệu và lệnh cần được giữ.
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2026"]
hook: "Báo cáo subagent trông như chỉ dẫn, agent coi là phát hiện"
tension: none
sides: []
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Kết quả subagent có dạng chỉ dẫn; harness cảnh báo, agent coi như phát hiện chứ không làm theo

**Bối cảnh:** Reviewer subagent trả về báo cáo dài.
**Chuyện gì xảy ra:** Báo cáo có dòng khớp mẫu chỉ dẫn nên harness gắn cảnh báo. Agent đọc phần đó như phát hiện để báo lại cho user, không làm theo.
**Bài học:** Đầu ra từ agent con là dữ liệu, không phải lệnh. Xử lý nó như mọi kết quả công cụ khác.
**Artefact:** Không có artefact đáng chụp.
