---
id: 2026-10-29-chi-nguoi-duyet-khong-chan-duoc-c455
code: M-RRPN
aliases: [M-RRPN]
date: 2026-10-29
repo: repo
status: raw
signals: [dao_quyet_dinh]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L1237", "claude:0faf0bb2#L1250", "claude:0faf0bb2#L1254", "claude:0faf0bb2#L1290", "claude:0faf0bb2#L1326", "claude:0faf0bb2#L1328", "claude:0faf0bb2#L2310", "claude:0faf0bb2#L2313"]
hook: "Đặt 'chỉ người duyệt', agent vẫn tự đóng việc trong 26 giây"
tension: cam_ma_van_lot
sides: ["Cấu hình reviewPolicy human_only tưởng đã chặn agent", "Agent chuyển done không ai duyệt, cổng thật nằm ở executionPolicy"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một bộ dựng công ty bằng AI agent đang thử Paperclip để giao việc cho agent qua issue, thay vì tự xây. Người làm đặt reviewPolicy 'human_only' và tin cờ này sẽ chặn agent tự chuyển việc sang done, nhưng agent vẫn đóng việc mà không ai duyệt. Hoá ra cờ đó chỉ áp khi trả lời xác nhận, còn cổng review thật nằm ở executionPolicy. Ai dựa vào tên trường để giữ bước duyệt của người cần biết điều này."
audience: dev dùng AI agent và muốn giữ bước duyệt của người
spine_context: "Bộ dựng công ty một người vận hành bằng AI agent, đang thử Paperclip như nền tảng giao việc cho agent qua issue."
spine_context_lines: [profile]
spine_want: "Muốn dùng Paperclip luôn, chỉ cần setup, không phải tự xây."
spine_want_lines: ["claude:0faf0bb2#L712"]
spine_obstacle: Issue đặt 'human_only' nhưng agent vẫn tự chuyển sang done.
spine_obstacle_lines: ["claude:0faf0bb2#L1326"]
spine_turn: "Tưởng reviewPolicy 'human_only' chặn được agent tự đóng việc; hoá ra cờ này chỉ áp khi trả lời xác nhận, còn cổng review thật là executionPolicy."
spine_turn_lines: ["claude:0faf0bb2#L1326", "claude:0faf0bb2#L2310"]
spine_action: "Đọc mã nguồn và tài liệu, rồi sửa lại kết luận và tài liệu so sánh."
spine_action_lines: ["claude:0faf0bb2#L2313", "claude:0faf0bb2#L2328"]
spine_outcome: Tài liệu đã sửa; executionPolicy chưa được chạy thử trên server đang chạy.
spine_outcome_lines: ["claude:0faf0bb2#L2328"]
spine_takeaway: "Đừng tin tên trường: đọc luật ở server và chạy thử đúng trường đó trước khi kết luận."
spine_takeaway_lines: ["claude:0faf0bb2#L2310"]
completeness: 7
---

# 'Chỉ người duyệt' không chặn được agent tự đóng việc; cổng thật là executionPolicy

**Góc kể:** Một bộ dựng công ty bằng AI agent đang thử Paperclip để giao việc cho agent qua issue, thay vì tự xây. Người làm đặt reviewPolicy 'human_only' và tin cờ này sẽ chặn agent tự chuyển việc sang done, nhưng agent vẫn đóng việc mà không ai duyệt. Hoá ra cờ đó chỉ áp khi trả lời xác nhận, còn cổng review thật nằm ở executionPolicy. Ai dựa vào tên trường để giữ bước duyệt của người cần biết điều này.
**Bối cảnh:** Một issue có reviewPolicy 'human_only' vẫn được agent chuyển sang done.
**Chuyện gì xảy ra:** Issue đặt reviewPolicy 'human_only' bị agent chuyển sang 'done' trong khoảng 26 giây mà không ai duyệt. Phân tích mã nguồn cho thấy reviewPolicy chỉ áp dụng khi trả lời một yêu cầu xác nhận, còn cổng review nhiều bước nằm ở executionPolicy. Trước đó đã kết luận Paperclip không có luồng review đáng tin, nên phải đính chính: server có chặn chuyển sang in_review khi thiếu đường duyệt (lỗi 422), và chỉ bước cuối được chấp nhận mới thành done. Phần đính chính này mới đọc từ mã, chưa chạy thử executionPolicy.
**Bài học:** Đừng tin tên trường. Đọc luật ở tầng máy chủ, chạy thử đúng trường đó, rồi mới kết luận về một cơ chế kiểm soát.
**Artefact:** Bảng lịch sử hoạt động của issue (thời điểm, trạng thái, người thực hiện). Che tên người và id.
