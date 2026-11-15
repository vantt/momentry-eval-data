---
id: 2026-10-29-phan-tich-lai-vi-sao-bridge-c455
code: M-ZDMQ
aliases: [M-ZDMQ]
date: 2026-10-29
repo: repo
status: raw
signals: [dao_quyet_dinh, so_truoc_so_sau]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:0faf0bb2#L657", "claude:0faf0bb2#L707", "claude:0faf0bb2#L1504"]
hook: "5 agent hỏi 'có việc không?' tốn 1.440 lượt LLM mỗi ngày"
tension: tuong_ma_hoa_ra
sides: ["Tưởng bridge chỉ là tuỳ chọn, heartbeat đủ dùng", "Heartbeat đốt 1.440 lượt LLM/ngày, vẫn trễ tới 60 phút"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Bộ dựng công ty một người chạy bằng AI agent, đang nối workspace trên Cloudflare D1 với agent trên máy cục bộ. Ban đầu người làm tưởng bridge chỉ là tuỳ chọn, vì agent tự kéo việc theo heartbeat là đủ. Hoá ra mỗi lần heartbeat kiểm tra inbox đều là một lượt gọi model dù không có việc: 5 agent mỗi 5 phút là khoảng 1.440 lượt mỗi ngày, lại trễ tới 60 phút. Ai thiết kế agent tự poll nên đo chi phí một lần thức dậy trước khi chọn kiến trúc."
audience: dev xây hệ thống giao việc cho agent AI
spine_context: "Bộ dựng công ty một người chạy bằng AI agent, đang nối workspace trên Cloudflare D1 với agent chạy trên máy cục bộ."
spine_context_lines: [profile]
spine_want: Muốn agent nhận việc từ D1 mà không cần server Node.
spine_want_lines: ["claude:0faf0bb2#L493"]
spine_obstacle: Gateway của agent chỉ nghe trên máy cục bộ nên Cloudflare không gọi tới được.
spine_obstacle_lines: ["claude:0faf0bb2#L707"]
spine_turn: "Tưởng bridge chỉ là tuỳ chọn vì agent tự kéo việc theo heartbeat là đủ; hoá ra mỗi lần heartbeat kiểm tra inbox đều tốn một lượt LLM, kể cả khi không có việc."
spine_turn_lines: ["claude:0faf0bb2#L657", "claude:0faf0bb2#L707"]
spine_action: "Đọc heartbeat-runner.ts rồi sửa lại kết luận: bridge vẫn cần, nhưng là một waker không dùng LLM."
spine_action_lines: ["claude:0faf0bb2#L660", "claude:0faf0bb2#L707"]
spine_outcome: Thiết kế được sửa thành ba tầng; chủ phiên hỏi tiếp về việc dùng Paperclip thay vì tự làm bridge.
spine_outcome_lines: ["claude:0faf0bb2#L707", "claude:0faf0bb2#L712"]
spine_takeaway: "Trước khi chọn kiến trúc poll, tính chi phí một lần thức dậy; một lượt LLM trả lời 'không' vẫn tốn tiền."
spine_takeaway_lines: ["claude:0faf0bb2#L707"]
completeness: 7
---

# Phân tích lại vì sao 'bridge chỉ là tuỳ chọn' là sai: heartbeat 60 phút và chi phí một lượt LLM mỗi lần kiểm tra

**Góc kể:** Bộ dựng công ty một người chạy bằng AI agent, đang nối workspace trên Cloudflare D1 với agent trên máy cục bộ. Ban đầu người làm tưởng bridge chỉ là tuỳ chọn, vì agent tự kéo việc theo heartbeat là đủ. Hoá ra mỗi lần heartbeat kiểm tra inbox đều là một lượt gọi model dù không có việc: 5 agent mỗi 5 phút là khoảng 1.440 lượt mỗi ngày, lại trễ tới 60 phút. Ai thiết kế agent tự poll nên đo chi phí một lần thức dậy trước khi chọn kiến trúc.
**Bối cảnh:** Câu hỏi của chủ: vì sao không cần bridge. Lúc đầu agent đã trả lời 'bridge chỉ còn là tuỳ chọn'.
**Chuyện gì xảy ra:** Kiểm tra heartbeat-runner.ts cho thấy OpenClaw chỉ bỏ qua lượt heartbeat khi HEARTBEAT.md rỗng. Nếu 5 agent kiểm tra inbox mỗi 5 phút sẽ tốn khoảng 1.440 lượt LLM mỗi ngày chỉ để trả lời 'không có việc', và phản hồi chậm tới 60 phút. Sau đó phải sửa lại: vẫn cần bridge, chỉ là bridge rất đơn giản, không dùng LLM.
**Bài học:** Kiểm tra chi phí của một lần 'thức dậy' trước khi chọn kiến trúc poll; một lượt LLM trả lời 'không' vẫn tốn tiền.
**Artefact:** Sơ đồ bridge ba tầng (waker không dùng LLM, heartbeat thưa, gateway) dạng ASCII.
