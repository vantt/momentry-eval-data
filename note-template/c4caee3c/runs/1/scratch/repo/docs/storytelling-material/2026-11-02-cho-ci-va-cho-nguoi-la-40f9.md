---
id: 2026-11-02-cho-ci-va-cho-nguoi-la-40f9
code: M-HSY6
aliases: [M-HSY6]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
signal_note: Thời gian chờ CI 10 đến 20 phút mỗi vòng sửa và thời gian chờ người duyệt là điểm nghẽn lớn hơn thời gian làm việc của agent.
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L2054", "claude:c4caee3c#L2064", "claude:c4caee3c#L2939", "claude:c4caee3c#L2951", "claude:c4caee3c#L3504", "claude:c4caee3c#L3510"]
hook: "Điểm nghẽn là CI và chờ người, mỗi lỗi CI tốn một lượt"
tension: khac
sides: ["Agent làm nhanh", "Vẫn kẹt chờ CI và chờ người"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chờ CI và chờ người là điểm nghẽn chính

**Bối cảnh:** Chủ dự án thấy tiến độ chậm và hỏi vì sao lâu như vậy.
**Chuyện gì xảy ra:** Chủ dự án yêu cầu bật thêm việc không cần chờ. Agent dọn worktree và chạy lại báo cáo. Agent cũng commit phần mã đã xong thay vì đợi báo cáo cuối, để nhánh vi-snippet-fix được merge sớm hơn. Mỗi lỗi CI cần một lượt chạy riêng.
**Bài học:** Tách phần không phụ thuộc người duyệt hoặc CI, và chạy song song những việc đó.
