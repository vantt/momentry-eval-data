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
tension: khac
sides: ["Ba lỗi trông như một mớ hỗn độn trong cùng một spike", "Mỗi lỗi chỉ ra đúng ranh giới giữa tầng điều phối và tầng chạy"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một dự án công ty một người vận hành bằng AI agent đang thử Paperclip để điều phối agent, và cần biết agent thật sự chạy theo cơ chế nào. Lúc đầu agent mô tả Paperclip chỉ là lớp điều phối, còn OpenClaw mới là nơi agent suy nghĩ. Đọc code thì Paperclip đi kèm trình chạy agent riêng và ẩn OpenClaw khỏi giao diện, nên mô tả cũ chưa đủ. Ai chọn công cụ điều phối cho agent nên kiểm tra xem nó có tự chạy agent hay không trước khi quyết định."
audience: dev dùng AI agent đang chọn công cụ điều phối
spine_context: "Một dự án công ty một người vận hành bằng AI agent, đang thử Paperclip và spike chạy trên máy để dựng một công ty mẫu."
spine_context_lines: [profile, "claude:0faf0bb2#L724"]
spine_want: Muốn biết agent thật sự chạy theo cơ chế của Paperclip hay của AICoworker/OpenClaw.
spine_want_lines: ["claude:0faf0bb2#L1515"]
spine_obstacle: Giao diện Paperclip không cho chọn OpenClaw như một adapter thông thường.
spine_obstacle_lines: ["claude:0faf0bb2#L1523"]
spine_turn: "Tưởng Paperclip chỉ là lớp điều phối, còn OpenClaw mới là nơi agent suy nghĩ. Hoá ra Paperclip đi kèm trình chạy agent riêng và ẩn OpenClaw khỏi giao diện."
spine_turn_lines: ["claude:0faf0bb2#L1519", "claude:0faf0bb2#L1574"]
spine_action: "Kiểm tra code giao diện và runtime của Paperclip, rồi cập nhật tài liệu spike."
spine_action_lines: ["claude:0faf0bb2#L1529", "claude:0faf0bb2#L1562"]
spine_outcome: Chưa chọn hướng đi. Người làm yêu cầu so sánh hai cách tiếp cận theo ba tiêu chí.
spine_outcome_lines: ["claude:0faf0bb2#L1576", "claude:0faf0bb2#L1584"]
spine_takeaway: "Trước khi chọn công cụ điều phối agent, kiểm tra xem nó có tự chạy agent hay không, đừng chỉ tin mô tả ban đầu."
spine_takeaway_lines: ["claude:0faf0bb2#L1574"]
completeness: 7
---

# Lỗi 'Gemini 3 Pro no longer available' và sự cố tự đóng task: hai bằng chứng cho ranh giới giữa lớp điều phối và lớp runtime

**Góc kể:** Một dự án công ty một người vận hành bằng AI agent đang thử Paperclip để điều phối agent, và cần biết agent thật sự chạy theo cơ chế nào. Lúc đầu agent mô tả Paperclip chỉ là lớp điều phối, còn OpenClaw mới là nơi agent suy nghĩ. Đọc code thì Paperclip đi kèm trình chạy agent riêng và ẩn OpenClaw khỏi giao diện, nên mô tả cũ chưa đủ. Ai chọn công cụ điều phối cho agent nên kiểm tra xem nó có tự chạy agent hay không trước khi quyết định.
**Bối cảnh:** Chủ hỏi agent chạy theo cơ chế của Paperclip hay AICoworker. Câu trả lời tách hai lớp: lớp điều phối và lớp suy nghĩ.
**Chuyện gì xảy ra:** Lỗi model thuộc OpenClaw, lỗi 422 khi chuyển in_review thiếu đường duyệt là luật của Paperclip, còn việc agent đoán bừa endpoint là do chưa có skill trong workspace OpenClaw. Ba lỗi cùng một lần spike cho thấy ranh giới rõ ràng.
**Bài học:** Khi agent hỏng, phân biệt lỗi thuộc lớp nào trước khi sửa; mỗi lớp có chủ và cách sửa riêng.
**Artefact:** Bảng 'việc nào thuộc bên nào' trong câu trả lời (không cần che).
