---
id: 2026-10-29-ngan-sach-0-dong-chan-moi-c455
code: M-S2TB
aliases: [M-S2TB]
date: 2026-10-29
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L1137", "claude:0faf0bb2#L1149", "claude:0faf0bb2#L1160", "claude:0faf0bb2#L1170", "claude:0faf0bb2#L1174", "claude:0faf0bb2#L1175", "claude:0faf0bb2#L1183"]
hook: "Đặt ngân sách để tiết kiệm, cả ba agent bị khóa im lặng"
tension: giup_ma_hai
sides: ["Đặt ngân sách tháng để kiểm soát chi phí", "Mọi lần đánh thức bị từ chối 409, giao diện không báo gì, comment chủ vô tác dụng 10 phút"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "fgOPC là bộ dựng công ty một người vận hành bằng AI agent, và người làm giao việc cho agent qua issue. Người làm đặt ngân sách tháng để kiểm soát chi phí, rồi tin rằng comment trên issue sẽ đánh thức agent khi cần. Hoá ra model chạy qua gói thuê bao không có bảng giá theo token, nên ngân sách không có giá đáng tin và mọi lần đánh thức bị từ chối 409 mà giao diện không báo gì. Ai đặt ngân sách cho agent trên gói thuê bao nên thử một lần đánh thức trước khi tin rằng agent đã sẵn sàng."
audience: dev đặt ngân sách cho AI agent trên gói thuê bao
spine_context: "fgOPC là bộ dựng công ty một người vận hành bằng AI agent, người làm giao việc cho các agent qua issue."
spine_context_lines: [profile]
spine_want: Đặt ngân sách tháng để kiểm soát chi phí cho các agent.
spine_want_lines: ["claude:0faf0bb2#L1174"]
spine_obstacle: "Mọi lần đánh thức bị từ chối 409, giao diện không báo gì, và comment của chủ không tạo run nào."
spine_obstacle_lines: ["claude:0faf0bb2#L1160", "claude:0faf0bb2#L1170"]
spine_turn: Tưởng comment trên issue sẽ đánh thức agent; hoá ra ngân sách không có giá đáng tin nên mọi lần đánh thức đều bị chặn.
spine_turn_lines: ["claude:0faf0bb2#L1138", "claude:0faf0bb2#L1160", "claude:0faf0bb2#L1170"]
spine_action: Đặt ngân sách về 0 cho cả ba agent rồi resume agent đang bị pause.
spine_action_lines: ["claude:0faf0bb2#L1174", "claude:0faf0bb2#L1184"]
spine_outcome: Run mới bắt đầu chạy (status running) sau khi resume; theo chuyện thì hoàn thành trong khoảng 53 giây.
spine_outcome_lines: ["claude:0faf0bb2#L1185"]
spine_takeaway: Kiểm tra cách ngân sách tính giá trước khi bật; thử một lần đánh thức trước khi tin agent đã sẵn sàng.
spine_takeaway_lines: ["claude:0faf0bb2#L1170"]
completeness: 7
---

# Ngân sách 0 đồng chặn mọi lần đánh thức agent, comment của chủ không đánh thức được

**Góc kể:** fgOPC là bộ dựng công ty một người vận hành bằng AI agent, và người làm giao việc cho agent qua issue. Người làm đặt ngân sách tháng để kiểm soát chi phí, rồi tin rằng comment trên issue sẽ đánh thức agent khi cần. Hoá ra model chạy qua gói thuê bao không có bảng giá theo token, nên ngân sách không có giá đáng tin và mọi lần đánh thức bị từ chối 409 mà giao diện không báo gì. Ai đặt ngân sách cho agent trên gói thuê bao nên thử một lần đánh thức trước khi tin rằng agent đã sẵn sàng.
**Bối cảnh:** Gói dùng model qua thuê bao không có bảng giá theo token, trong khi công cụ điều phối cần giá để tính ngân sách.
**Chuyện gì xảy ra:** Sau khi đặt ngân sách tháng cho agent, mọi lần đánh thức bị từ chối với lỗi 409 'no reliable price' và không có thông báo nào trên giao diện. Comment của chủ trên issue không tạo run nào trong hơn 10 phút, và agent Marketing vẫn ở trạng thái paused với lý do budget. Cách sửa là đặt ngân sách về 0 cho cả ba agent rồi resume. Sau đó run mới chạy và hoàn thành trong khoảng 53 giây.
**Bài học:** Kiểm tra cách ngân sách tính giá trước khi bật. Với gói thuê bao, lỗi chặn có thể âm thầm, nên thử một lần đánh thức trước khi tin rằng agent đã sẵn sàng.
**Artefact:** Ảnh thông báo 409 'cannot start work because recorded usage has no reliable price'. Che tên công ty nếu có.
