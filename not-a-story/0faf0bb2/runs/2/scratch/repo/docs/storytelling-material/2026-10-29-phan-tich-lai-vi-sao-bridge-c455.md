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
sides: ["Tưởng cầu nối chỉ là tuỳ chọn, heartbeat là đủ", "Heartbeat chậm tới 60 phút hoặc đốt 1.440 lượt LLM/ngày; vẫn cần cầu nối, chỉ cần loại đơn giản không dùng LLM"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Người làm đang dựng bộ công ty một người (OPC) chạy bằng agent, muốn bỏ server Node và giữ trạng thái việc trên Cloudflare D1. Agent từng nói cầu nối chỉ còn là tuỳ chọn, vì agent tự kéo việc theo heartbeat là đủ. Kiểm tra lại thì mỗi lần heartbeat kiểm tra inbox là một lượt LLM, có thể trễ tới 60 phút, nên vẫn cần một cầu nối đơn giản không dùng LLM. Dev tự host agent nên quan tâm vì chi phí của việc 'thức dậy để hỏi' thường bị bỏ qua."
audience: dev tự host hệ thống agent
spine_context: "Đang dựng bộ công ty một người (OPC) chạy bằng agent, muốn bỏ server Node và giữ trạng thái việc trên Cloudflare D1."
spine_context_lines: [profile, "claude:0faf0bb2#L493"]
spine_want: Agent nhận việc từ D1 mà không cần chạy server Node.
spine_want_lines: ["claude:0faf0bb2#L493"]
spine_obstacle: "Cloudflare không gọi trực tiếp được gateway OpenClaw chạy cục bộ, và mỗi lần heartbeat kiểm tra inbox là một lượt LLM."
spine_obstacle_lines: ["claude:0faf0bb2#L707"]
spine_turn: "Tưởng bridge chỉ còn là tuỳ chọn vì agent tự kéo việc từ D1 là đủ; hoá ra heartbeat mặc định chậm tới 60 phút và mỗi lần kiểm tra tốn một lượt LLM, nên vẫn cần một bridge đơn giản không dùng LLM."
spine_turn_lines: ["claude:0faf0bb2#L657", "claude:0faf0bb2#L707"]
spine_action: "Kiểm tra heartbeat-runner.ts, thấy lượt heartbeat chỉ bị bỏ qua khi HEARTBEAT.md rỗng; rồi đề xuất bridge ba tầng với waker không dùng LLM."
spine_action_lines: ["claude:0faf0bb2#L659", "claude:0faf0bb2#L707"]
spine_outcome: "Agent sửa câu trả lời: vẫn cần bridge, chỉ là loại không dùng LLM; ước tính 5 agent kiểm tra mỗi 5 phút sẽ tốn khoảng 1.440 lượt LLM mỗi ngày nếu không có waker."
spine_outcome_lines: ["claude:0faf0bb2#L707"]
spine_takeaway: "Trước khi chọn kiến trúc poll, hãy tính chi phí của mỗi lần agent thức dậy; một lượt LLM trả lời 'không có việc' vẫn tốn tiền."
spine_takeaway_lines: ["claude:0faf0bb2#L707"]
completeness: 7
---

# Phân tích lại vì sao 'bridge chỉ là tuỳ chọn' là sai: heartbeat 60 phút và chi phí một lượt LLM mỗi lần kiểm tra

**Góc kể:** Người làm đang dựng bộ công ty một người (OPC) chạy bằng agent, muốn bỏ server Node và giữ trạng thái việc trên Cloudflare D1. Agent từng nói cầu nối chỉ còn là tuỳ chọn, vì agent tự kéo việc theo heartbeat là đủ. Kiểm tra lại thì mỗi lần heartbeat kiểm tra inbox là một lượt LLM, có thể trễ tới 60 phút, nên vẫn cần một cầu nối đơn giản không dùng LLM. Dev tự host agent nên quan tâm vì chi phí của việc 'thức dậy để hỏi' thường bị bỏ qua.
**Bối cảnh:** Câu hỏi của chủ: vì sao không cần bridge. Lúc đầu agent đã trả lời 'bridge chỉ còn là tuỳ chọn'.
**Chuyện gì xảy ra:** Kiểm tra heartbeat-runner.ts cho thấy OpenClaw chỉ bỏ qua lượt heartbeat khi HEARTBEAT.md rỗng. Nếu 5 agent kiểm tra inbox mỗi 5 phút sẽ tốn khoảng 1.440 lượt LLM mỗi ngày chỉ để trả lời 'không có việc', và phản hồi chậm tới 60 phút. Sau đó phải sửa lại: vẫn cần bridge, chỉ là bridge rất đơn giản, không dùng LLM.
**Bài học:** Kiểm tra chi phí của một lần 'thức dậy' trước khi chọn kiến trúc poll; một lượt LLM trả lời 'không' vẫn tốn tiền.
**Artefact:** Sơ đồ bridge ba tầng (waker không dùng LLM, heartbeat thưa, gateway) dạng ASCII.
