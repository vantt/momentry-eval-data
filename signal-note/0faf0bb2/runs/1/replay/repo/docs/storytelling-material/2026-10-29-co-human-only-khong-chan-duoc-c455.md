---
id: 2026-10-29-co-human-only-khong-chan-duoc-c455
code: M-4MCW
aliases: [M-4MCW]
date: 2026-10-29
repo: repo
status: raw
signals: [dao_quyet_dinh, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L1326", "claude:0faf0bb2#L1327", "claude:0faf0bb2#L2310", "claude:0faf0bb2#L2313"]
hook: "Đặt cờ 'chỉ người duyệt', agent vẫn tự đóng việc được"
tension: cam_ma_van_lot
sides: ["Đã đặt reviewPolicy human_only", "Agent vẫn tự chuyển việc sang done"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một người đang dựng công ty một người vận hành bằng đội agent AI, và thử Paperclip làm nền để xem có dùng được không. Họ đặt cờ 'chỉ người duyệt' cho một việc, tưởng như vậy là đủ để agent không tự đóng được việc đó. Nhưng agent vẫn chuyển việc sang done; cờ đó chỉ áp khi trả lời một lời xin xác nhận, còn cổng thật là một chuỗi bước kiểm duyệt riêng. Ai tin vào tên cờ mà không thử thì có thể để lọt đúng việc cần chặn."
audience: dev dựng agent AI và thử công cụ điều phối việc agent
spine_context: "Dự án dựng công ty một người vận hành bằng đội agent AI, đang thử Paperclip làm nền."
spine_context_lines: [profile]
spine_want: "Xem Paperclip có dùng được luôn làm nền không, qua một spike chạy trên máy và một công ty mẫu."
spine_want_lines: ["claude:0faf0bb2#L712", "claude:0faf0bb2#L724"]
spine_obstacle: "Spike đặt cờ 'chỉ người duyệt' cho một việc, nhưng agent vẫn chuyển việc đó sang done."
spine_obstacle_lines: ["claude:0faf0bb2#L1326"]
spine_turn: "Tưởng cờ reviewPolicy human_only chặn được agent tự đóng việc; hoá ra cờ này chỉ áp khi trả lời một lời xin xác nhận, còn cổng thật là executionPolicy."
spine_turn_lines: ["claude:0faf0bb2#L2310"]
spine_action: "Đọc lại tài liệu execution-semantics, đính chính lesson, bảng so sánh và báo cáo spike."
spine_action_lines: ["claude:0faf0bb2#L2306", "claude:0faf0bb2#L2312", "claude:0faf0bb2#L2313"]
spine_outcome: Paperclip cứng ở việc đóng task khi có executionPolicy; spike chưa kiểm chứng điều này và đã có 51 lessons sau khi cập nhật.
spine_outcome_lines: ["claude:0faf0bb2#L2328"]
spine_takeaway: Đừng tin vào tên cờ; thử cơ chế bắt buộc đi qua để biết nó có thật sự chặn không.
spine_takeaway_lines: ["claude:0faf0bb2#L2310"]
completeness: 7
---

# Cờ 'human_only' không chặn được agent tự đóng việc: reviewPolicy khác executionPolicy

**Góc kể:** Một người đang dựng công ty một người vận hành bằng đội agent AI, và thử Paperclip làm nền để xem có dùng được không. Họ đặt cờ 'chỉ người duyệt' cho một việc, tưởng như vậy là đủ để agent không tự đóng được việc đó. Nhưng agent vẫn chuyển việc sang done; cờ đó chỉ áp khi trả lời một lời xin xác nhận, còn cổng thật là một chuỗi bước kiểm duyệt riêng. Ai tin vào tên cờ mà không thử thì có thể để lọt đúng việc cần chặn.
**Bối cảnh:** Sau khi SEN-3 bị đóng bởi agent, mình kết luận Paperclip không có cổng review và viết điều đó vào báo cáo.
**Chuyện gì xảy ra:** Đọc lại execution-semantics thì reviewPolicy chỉ áp dụng khi trả lời một lời xin xác nhận, còn cổng review thật là executionPolicy.stages. Spike trước đó mới chỉ bật cờ đầu, nên kết luận cũ bị đính chính: Paperclip chỉ cứng ở việc đóng task khi có executionPolicy.
**Bài học:** Phân biệt cờ 'ai được duyệt' với cơ chế 'bắt buộc đi qua', và kiểm chứng bằng cách thử thay vì đọc tên cờ.
**Artefact:** Bảng hai cơ chế, cột 'áp dụng khi nào' và 'chặn được gì'.
