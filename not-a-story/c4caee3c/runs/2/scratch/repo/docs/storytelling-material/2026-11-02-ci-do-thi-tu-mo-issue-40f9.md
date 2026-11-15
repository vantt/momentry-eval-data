---
id: 2026-11-02-ci-do-thi-tu-mo-issue-40f9
code: M-8PMJ
aliases: [M-8PMJ]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L1796", "claude:c4caee3c#L3398", "claude:c4caee3c#L3405", "claude:c4caee3c#L3874"]
hook: "CI đỏ tự mở issue, xanh thì tự đóng kèm nguyên nhân"
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

# CI đỏ thì tự mở issue, đóng kèm nguyên nhân khi xanh

**Bối cảnh:** Workflow catchup mở một issue khi hỏng, hoặc bình luận vào issue đã mở.
**Chuyện gì xảy ra:** Issue đầu được dùng để kiểm chỗ hỏng cố ý. Sau đó mỗi lần CI đỏ thêm một issue, tổng ba issue (#2, #3, #5). Khi run xanh, agent đóng từng issue kèm bình luận ghi nguyên nhân và commit sửa.
**Bài học:** Issue tự động là kênh báo hỏng tốt, nhưng cần đóng kèm nguyên nhân để lịch sử còn đọc được.
**Artefact:** Danh sách issue đã che tên repo.
