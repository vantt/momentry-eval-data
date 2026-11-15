---
id: 2026-10-29-paperclip-tu-co-runtime-ui-giau-c455
code: M-1NDF
aliases: [M-1NDF]
date: 2026-10-29
repo: repo
status: raw
signals: [dao_quyet_dinh]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:0faf0bb2#L1515", "claude:0faf0bb2#L1519", "claude:0faf0bb2#L1523", "claude:0faf0bb2#L1533", "claude:0faf0bb2#L1548", "claude:0faf0bb2#L1550", "claude:0faf0bb2#L1551", "claude:0faf0bb2#L1574"]
hook: "Paperclip giấu OpenClaw khỏi UI, vì nó đã tự có runtime"
tension: tuong_ma_hoa_ra
sides: ["Ghép Paperclip với AICoworker tưởng là một hệ thống", "Thực chất là hai runtime, OpenClaw bị gắn comingSoon và hỗ trợ kém nhất"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "fgOPC là bộ dựng công ty một người chạy bằng AI agent, và người làm đang thử Paperclip để dựng một công ty mẫu trên máy mình. Ban đầu người làm tin Paperclip chỉ là lớp điều phối: nó quyết định việc gì, khi nào, còn agent chạy ở AICoworker/OpenClaw. Khi không thấy OpenClaw trong màn tạo agent, mã nguồn cho thấy Paperclip tự có runtime riêng và ẩn adapter OpenClaw, nên ghép hai hệ thống thực chất là hai runtime. Ai đang chọn nền tảng cho agent nên đọc bảng adapter hiển thị trong UI, đừng chỉ đọc mô tả."
audience: dev đang chọn nền tảng để chạy nhiều AI agent
spine_context: fgOPC là bộ dựng công ty một người chạy bằng AI agent; người làm đang thử Paperclip để dựng công ty mẫu trên máy.
spine_context_lines: [profile, "claude:0faf0bb2#L724"]
spine_want: Muốn chọn nền tảng agent và dựng một công ty mẫu để thử.
spine_want_lines: ["claude:0faf0bb2#L724"]
spine_obstacle: "Màn tạo agent của Paperclip không có lựa chọn OpenClaw, chỉ có các adapter khác."
spine_obstacle_lines: ["claude:0faf0bb2#L1523"]
spine_turn: Tưởng Paperclip chỉ điều phối đứng trên runtime; hoá ra nó tự có runtime và adapter OpenClaw bị ẩn.
spine_turn_lines: ["claude:0faf0bb2#L1519", "claude:0faf0bb2#L1574"]
spine_action: "Đọc mã UI và bảng adapter, ghi phát hiện vào ghi chú spike."
spine_action_lines: ["claude:0faf0bb2#L1533", "claude:0faf0bb2#L1551", "claude:0faf0bb2#L1562"]
spine_outcome: Người làm chưa chọn; agent đang so sánh hai cách tiếp cận theo ba tiêu chí.
spine_outcome_lines: ["claude:0faf0bb2#L1576", "claude:0faf0bb2#L1584"]
spine_takeaway: "Trước khi chọn nền tảng, kiểm tra bảng hiển thị adapter trong UI, không chỉ đọc mô tả."
spine_takeaway_lines: ["claude:0faf0bb2#L1574"]
completeness: 7
---

# Paperclip tự có runtime, UI giấu adapter OpenClaw

**Góc kể:** fgOPC là bộ dựng công ty một người chạy bằng AI agent, và người làm đang thử Paperclip để dựng một công ty mẫu trên máy mình. Ban đầu người làm tin Paperclip chỉ là lớp điều phối: nó quyết định việc gì, khi nào, còn agent chạy ở AICoworker/OpenClaw. Khi không thấy OpenClaw trong màn tạo agent, mã nguồn cho thấy Paperclip tự có runtime riêng và ẩn adapter OpenClaw, nên ghép hai hệ thống thực chất là hai runtime. Ai đang chọn nền tảng cho agent nên đọc bảng adapter hiển thị trong UI, đừng chỉ đọc mô tả.
**Bối cảnh:** Trước đó mô tả Paperclip là lớp điều phối đứng trên runtime, chỉ quyết định việc gì và khi nào.
**Chuyện gì xảy ra:** Người dùng thấy màn tạo agent không cho chọn OpenClaw. Mã nguồn cho thấy adapter OpenClaw bị gắn 'comingSoon' và ẩn khỏi danh sách, mọi khả năng trên UI (chỉ dẫn, skill, chọn model) đều tắt. Đồng thời Paperclip có runner Rust tự chạy các CLI agent. Hệ quả là ghép Paperclip với AICoworker thực chất là hai runtime, và OpenClaw là lựa chọn được hỗ trợ kém nhất.
**Bài học:** Tài liệu có thể mô tả 'chỉ điều phối' trong khi giao diện đã ẩn runtime của bạn. Trước khi chọn nền tảng, kiểm tra bảng hiển thị adapter, không chỉ đọc mô tả.
**Artefact:** Ảnh danh sách chọn adapter không có OpenClaw, đặt cạnh đoạn mã cấu hình ẩn. Không cần che.
