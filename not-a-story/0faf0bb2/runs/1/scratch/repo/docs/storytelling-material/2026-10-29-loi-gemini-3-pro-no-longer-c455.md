---
id: 2026-10-29-loi-gemini-3-pro-no-longer-c455
code: M-8SHY
aliases: [M-8SHY]
date: 2026-10-29
repo: repo
status: raw
signals: [rang_buoc_thiet_ke, khac]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L1519", "claude:0faf0bb2#L1574"]
hook: "Ba lỗi trong một lần thử, mỗi lỗi thuộc một tầng khác nhau"
tension: tuong_ma_hoa_ra
sides: ["Tưởng ba lỗi là một đống hỏng chung", "Mỗi lỗi thuộc một lớp: model, luật duyệt, thiếu skill"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án dựng công ty một người bằng AI agent đang thử Paperclip trên máy, và cần biết agent thật sự chạy ở đâu. Lúc đầu câu trả lời mô tả Paperclip chỉ là lớp điều phối, còn suy nghĩ diễn ra ở OpenClaw. Khi đọc code, hoá ra Paperclip có runtime riêng để chạy các CLI agent, và OpenClaw bị ẩn khỏi màn hình thêm agent. Ai chọn công cụ cho agent nên kiểm tra xem nó có tự chạy agent hay không trước khi quyết định."
audience: dev dựng hệ thống agent cho công ty một người
spine_context: Dự án dựng công ty một người vận hành bằng AI agent; đang chạy spike thử Paperclip trên máy để dựng một công ty mẫu.
spine_context_lines: [profile, "claude:0faf0bb2#L724"]
spine_want: "Muốn chọn giữa Paperclip và AICoworker/OpenClaw để chạy agent, xem bên nào tổ chức, lưu artifact và chat tốt hơn."
spine_want_lines: ["claude:0faf0bb2#L724", "claude:0faf0bb2#L1576"]
spine_obstacle: "Giao diện Paperclip không cho chọn OpenClaw trực tiếp, nên không rõ agent thật sự chạy ở đâu."
spine_obstacle_lines: ["claude:0faf0bb2#L1523"]
spine_turn: Tưởng Paperclip chỉ điều phối còn agent chạy ở OpenClaw; hoá ra Paperclip có runtime riêng và OpenClaw bị ẩn khỏi UI.
spine_turn_lines: ["claude:0faf0bb2#L1519", "claude:0faf0bb2#L1574"]
spine_action: "Đọc code UI và adapter, rồi sửa tài liệu spike theo đó."
spine_action_lines: ["claude:0faf0bb2#L1529", "claude:0faf0bb2#L1562"]
spine_outcome: "Mô tả Paperclip được sửa từ 'chỉ điều phối' sang 'có runtime riêng'; hai hướng được nêu, chủ chưa chọn."
spine_outcome_lines: ["claude:0faf0bb2#L1574", "claude:0faf0bb2#L1576"]
spine_takeaway: "Trước khi tin một công cụ chỉ điều phối, kiểm tra xem nó có tự chạy agent không."
spine_takeaway_lines: ["claude:0faf0bb2#L1574"]
completeness: 7
---

# Lỗi 'Gemini 3 Pro no longer available' và sự cố tự đóng task: hai bằng chứng cho ranh giới giữa lớp điều phối và lớp runtime

**Góc kể:** Dự án dựng công ty một người bằng AI agent đang thử Paperclip trên máy, và cần biết agent thật sự chạy ở đâu. Lúc đầu câu trả lời mô tả Paperclip chỉ là lớp điều phối, còn suy nghĩ diễn ra ở OpenClaw. Khi đọc code, hoá ra Paperclip có runtime riêng để chạy các CLI agent, và OpenClaw bị ẩn khỏi màn hình thêm agent. Ai chọn công cụ cho agent nên kiểm tra xem nó có tự chạy agent hay không trước khi quyết định.
**Bối cảnh:** Chủ hỏi agent chạy theo cơ chế của Paperclip hay AICoworker. Câu trả lời tách hai lớp: lớp điều phối và lớp suy nghĩ.
**Chuyện gì xảy ra:** Lỗi model thuộc OpenClaw, lỗi 422 khi chuyển in_review thiếu đường duyệt là luật của Paperclip, còn việc agent đoán bừa endpoint là do chưa có skill trong workspace OpenClaw. Ba lỗi cùng một lần spike cho thấy ranh giới rõ ràng.
**Bài học:** Khi agent hỏng, phân biệt lỗi thuộc lớp nào trước khi sửa; mỗi lớp có chủ và cách sửa riêng.
**Artefact:** Bảng 'việc nào thuộc bên nào' trong câu trả lời (không cần che).
