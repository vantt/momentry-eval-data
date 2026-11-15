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
hook: "Quy tắc 6 điểm qua 215 rule lint, nhưng chưa ai thử dùng thật"
tension: tuong_ma_hoa_ra
sides: ["Lint và kiểm tra đường dẫn đều qua, 215 rule xanh", "Chỉ mới kiểm hình thức, chưa có bằng chứng quy tắc chạy đúng"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "Chủ đang làm một skill chung về đóng gói và phân phối (cài, cập nhật, cấu hình, kiểm tra) cho các dự án của mình; dự án momentry vừa thêm một quy tắc cấu hình mới."
spine_context_lines: ["claude:6a207191#L5", "claude:6a207191#L2255"]
spine_want: "Muốn biết skill đã có quy chuẩn 'mọi cài đặt đổi qua config' của momentry chưa, và thêm vào nếu thiếu."
spine_want_lines: ["claude:6a207191#L2255", "claude:6a207191#L2333"]
spine_obstacle: Skill chỉ có các mảnh rời về config; quy tắc chính thì thiếu.
spine_obstacle_lines: ["claude:6a207191#L2324"]
spine_action: "Đọc commit de173ef của momentry, đối chiếu sáu điểm với skill, thêm CMD-22..24, nâng CFG-12 lên MUST, sửa UX-17 và thêm dòng tham chiếu, rồi chạy lint và kiểm tra đường dẫn."
spine_action_lines: ["claude:6a207191#L2281", "claude:6a207191#L2385"]
spine_outcome: "Lint qua với 215 quy tắc, tăng 3; mọi đường dẫn tham chiếu đều có trên GitHub; bản gửi lên hub đã được người dùng duyệt."
spine_outcome_lines: ["claude:6a207191#L2385", "claude:6a207191#L2404", "claude:6a207191#L2417"]
spine_takeaway: "Khi một dự án thêm quy tắc mới, nên đối chiếu nó với skill chung ngay; khoá chỉ dành cho máy không được ghi vào file của repo."
spine_takeaway_lines: ["claude:6a207191#L2324"]
completeness: 6
---

# Thêm quy tắc config một cửa vào skill sau khi đọc thay đổi của momentry

**Bối cảnh:** Chủ hỏi skill đã có quy chuẩn 'mọi cài đặt đổi qua config, kể cả cài đặt riêng dự án' của momentry chưa. Agent đối chiếu và thấy thiếu.
**Chuyện gì xảy ra:** Quy tắc mới của momentry (commit de173ef, một ngày trước) gồm 6 điểm: một cửa config, cờ --project, khoá chỉ máy không ghi vào file repo, không tự bật dự án, giao diện web gọi đúng hàm ghi CLI. Skill được thêm CMD-22..24, nâng CFG-12 lên MUST. Lint và kiểm tra đường dẫn đều qua (215 rule), rồi gửi lên hub.
**Bài học:** Quy chuẩn mới của một dự án nên được đối chiếu với skill chung ngay sau khi có, và khoá 'chỉ máy' không bao giờ được vào file của repo.
**Artefact:** Bảng đối chiếu sáu quy tắc momentry với skill (đánh giá thiếu/có).
**Góc người ngoài:** cách làm phổ biến là Thường người ta copy nguyên văn quy tắc mới vào tài liệu, hoặc thêm một dòng rồi thôi; ít khi có bước đối chiếu có bảng và kiểm tra tham chiếu tự động; ở đây khác ở Quy tắc được gắn đúng chỗ, không trùng lặp, và tham chiếu luôn còn hiệu lực. Người đọc muốn biết cách làm bảng đối chiếu này và cách kiểm tra đường dẫn tự động, vì họ thường bị tài liệu lệch khỏi code mà không hay biết.
