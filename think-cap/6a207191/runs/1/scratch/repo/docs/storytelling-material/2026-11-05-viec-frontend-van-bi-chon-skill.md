---
id: 2026-11-05-viec-frontend-van-bi-chon-skill
date: 2026-11-05
repo: repo
status: raw
signals: [khác, người duyệt]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:6a207191#L1520", "claude:6a207191#L1538", "claude:6a207191#L1543", "claude:6a207191#L1555"]
hook: "Skill bị trừ điểm vì not_for, vẫn thắng nhờ chữ 'install'"
tension: cam_ma_van_lot
sides: ["Tiêu chí not_for đã trừ điểm skill đóng gói", "Chữ 'install' xuất hiện nhiều nên nó vẫn thắng việc frontend"]
strength: 3
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Việc frontend vẫn bị chọn skill đóng gói: từ 'install' kéo sai, hub trừ điểm mà vẫn thắng

**Bối cảnh:** Người dùng nhờ skill-curator thêm việc frontend vào hub. Agent gọi skill_resolve, kết quả đầu là cs-packaging-distribution với độ tin cậy trung bình, tức là chọn nhầm cho việc giao diện.
**Chuyện gì xảy ra:** Agent từ chối và hỏi lại. Lần hai hub báo không có skill nào khớp. Tiêu chí not_for đã bị trừ điểm nhưng skill đóng gói vẫn thắng, vì chữ 'install' xuất hiện nhiều trong skill. Agent đề xuất thêm not_for về giao diện và các counter_examples.
**Bài học:** Từ khoá chung như 'install' kéo theo nhiều việc không liên quan. Hãy viết counter_examples cho đúng những câu dễ nhầm và thử lại chính các câu đó.
**Artefact:** Bảng câu đối chứng và kết quả chọn skill, đã che id.
