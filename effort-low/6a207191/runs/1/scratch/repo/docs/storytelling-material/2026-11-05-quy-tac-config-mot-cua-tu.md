---
id: 2026-11-05-quy-tac-config-mot-cua-tu
date: 2026-11-05
repo: repo
status: raw
signals: [ràng buộc thiết kế, khác]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:6a207191#L2255", "claude:6a207191#L2264", "claude:6a207191#L2270", "claude:6a207191#L2294", "claude:6a207191#L2324", "claude:6a207191#L2358", "claude:6a207191#L2385", "claude:6a207191#L2393", "claude:6a207191#L2407"]
hook: "Quy tắc config 'một cửa' còn thiếu, thêm 3 rule mới thành bắt buộc"
tension: none
sides: []
strength: 0
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Quy tắc config 'một cửa' từ dự án khác: skill thiếu, thêm thành MUST

**Bối cảnh:** Một dự án khác (momentry) vừa thêm quy tắc config trong một commit. User hỏi skill đã có quy chuẩn này chưa.
**Chuyện gì xảy ra:** Quy tắc: mọi cài đặt đổi qua lệnh config, cài đặt riêng dự án dùng cùng lệnh với --project, và giao diện web gọi đúng hàm ghi của CLI. Khoá của máy như budget, private hay paused không được ghi vào file repo, và bị bỏ qua khi đọc từ file đó. Skill chỉ có vài mảnh rời. Agent thêm CMD-22 đến CMD-24, nâng CFG-12 lên MUST và thêm UX-17. Lint qua 215 rule. Vì commit chưa có bản phát hành nên agent ghi là chưa được chứng minh.
**Bài học:** Ràng buộc bảo mật như khoá của máy không được vào file repo đã clone là lý do thiết kế đáng giữ. Quy chuẩn rút từ dự án thật nên đi kèm test và trạng thái đã chứng minh hay chưa.
**Artefact:** Bảng 6 quy tắc: quy tắc, skill hiện có, đánh giá. Không dán nội dung dự án.
