---
id: 2026-11-05-them-quy-tac-config-mot-cua-c4b4
code: M-KJJF
aliases: [M-KJJF]
date: 2026-11-05
repo: repo
status: raw
signals: [rang_buoc_thiet_ke, nguoi_duyet_may_soan]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:6a207191#L2255", "claude:6a207191#L2293", "claude:6a207191#L2324", "claude:6a207191#L2333", "claude:6a207191#L2385", "claude:6a207191#L2393", "claude:6a207191#L2407"]
hook: "Lint qua 215 rule, nhưng skill vẫn phải học lại luật config mới"
tension: none
sides: []
strength: 0
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Thêm quy tắc config một cửa vào skill sau khi đọc thay đổi của momentry

**Bối cảnh:** Chủ hỏi skill đã có quy chuẩn 'mọi cài đặt đổi qua config, kể cả cài đặt riêng dự án' của momentry chưa. Agent đối chiếu và thấy thiếu.
**Chuyện gì xảy ra:** Quy tắc mới của momentry (commit de173ef, một ngày trước) gồm 6 điểm: một cửa config, cờ --project, khoá chỉ máy không ghi vào file repo, không tự bật dự án, giao diện web gọi đúng hàm ghi CLI. Skill được thêm CMD-22..24, nâng CFG-12 lên MUST. Lint và kiểm tra đường dẫn đều qua (215 rule), rồi gửi lên hub.
**Bài học:** Quy chuẩn mới của một dự án nên được đối chiếu với skill chung ngay sau khi có, và khoá 'chỉ máy' không bao giờ được vào file của repo.
**Artefact:** Bảng đối chiếu sáu quy tắc momentry với skill (đánh giá thiếu/có).
**Góc người ngoài:** cách làm phổ biến là Thường người ta copy nguyên văn quy tắc mới vào tài liệu, hoặc thêm một dòng rồi thôi; ít khi có bước đối chiếu có bảng và kiểm tra tham chiếu tự động; ở đây khác ở Quy tắc được gắn đúng chỗ, không trùng lặp, và tham chiếu luôn còn hiệu lực. Người đọc muốn biết cách làm bảng đối chiếu này và cách kiểm tra đường dẫn tự động, vì họ thường bị tài liệu lệch khỏi code mà không hay biết.
