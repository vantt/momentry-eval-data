---
id: 2026-10-29-thu-tri-nho-agent-hoi-agent-c455
code: M-G5TG
aliases: [M-G5TG]
date: 2026-10-29
repo: repo
status: raw
signals: [artefact_nhin_duoc, khac]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:0faf0bb2#L2931", "claude:0faf0bb2#L2940", "claude:0faf0bb2#L2949", "claude:0faf0bb2#L2952"]
hook: "Nhét mật mã vào MEMORY.md để kiểm tra agent có đọc workspace"
tension: none
sides: []
strength: 0
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Thử trí nhớ agent: hỏi agent mật mã trong MEMORY.md để kiểm tra workspace

**Bối cảnh:** Tạo agent Mai thứ hai bằng cách sao chép cấu trúc agent của AICoworker, với workspace riêng.
**Chuyện gì xảy ra:** Mình thêm một mật mã thử vào MEMORY.md và một dòng chữ ký vào SOUL.md, rồi gọi openclaw agent --agent mai. Agent trả đúng mật mã và chữ ký, chứng minh nó đọc được workspace. Các dòng thử sau đó phải được xoá khỏi SOUL và MEMORY trước khi dùng thật.
**Bài học:** Kiểm bộ nhớ của agent bằng một câu hỏi có đáp án đã biết, nhưng nhớ xoá dữ liệu thử.
**Artefact:** Câu trả lời của agent, che mật mã thử.
