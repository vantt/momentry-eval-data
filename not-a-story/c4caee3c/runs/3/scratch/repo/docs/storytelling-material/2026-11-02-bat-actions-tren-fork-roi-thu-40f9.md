---
id: 2026-11-02-bat-actions-tren-fork-roi-thu-40f9
code: M-8W1R
aliases: [M-8W1R]
date: 2026-11-02
repo: repo
status: raw
signals: [khac, dao_quyet_dinh]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L264", "claude:c4caee3c#L267", "claude:c4caee3c#L275", "claude:c4caee3c#L276", "claude:c4caee3c#L288"]
hook: "Lệnh tắt workflow báo 403, nhưng chúng đã tắt sẵn"
tension: none
sides: []
strength: 0
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Bật Actions trên fork rồi thử tắt workflow upstream và nhận 403

**Bối cảnh:** Người dùng hỏi Actions có phải để tự chạy catchup không, rồi bảo bật luôn. Trước đó fork đang tắt Actions và Issues theo PRD.
**Chuyện gì xảy ra:** Agent bật Actions với allowed_actions=all rồi gọi disable cho bốn workflow upstream. Lệnh tắt báo 403 'không active', nhưng khi liệt kê thì các workflow đã ở trạng thái disabled_manually sẵn.
**Bài học:** Trước khi bật tính năng có thể tự chạy trên fork, liệt kê workflow và kiểm trạng thái thật. Đừng tin một lệnh tắt báo lỗi.
**Artefact:** Kết quả gh workflow list đã che tên repo.
