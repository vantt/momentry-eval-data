---
id: 2026-10-29-heartbeat-cua-openclaw-ton-mot-luot-c455
code: M-E3A1
aliases: [M-E3A1]
date: 2026-10-29
repo: repo
status: raw
signals: [dao_quyet_dinh, so_truoc_so_sau]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:0faf0bb2#L657", "claude:0faf0bb2#L659", "claude:0faf0bb2#L671", "claude:0faf0bb2#L682", "claude:0faf0bb2#L686", "claude:0faf0bb2#L707"]
hook: "5 agent kiểm tra mỗi 5 phút: 1.440 lượt gọi model, gần hết là 'không có việc'"
tension: nho_ma_to
sides: ["Heartbeat nghe như nhịp kiểm tra nhẹ", "Mỗi nhịp là một lượt LLM, khoảng 1.440 lượt mỗi ngày"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Bộ dựng công ty một người chạy bằng đội agent AI đang chọn cách agent nhận việc. Người làm tin rằng bridge chỉ còn là tuỳ chọn vì agent tự kéo việc, nhưng heartbeat của OpenClaw tốn một lượt LLM mỗi nhịp khi file kiểm tra không rỗng: 5 agent mỗi 5 phút là khoảng 1.440 lượt mỗi ngày. Ai chọn kiểu pull cho agent nên đo chi phí vòng kiểm tra trước khi bỏ bridge."
audience: "dev xây hệ thống agent tự động hoá, đang chọn kiểu pull hay push"
spine_context: Bộ dựng công ty một người chạy bằng đội agent AI; đang chọn cách agent nhận việc.
spine_context_lines: [profile]
spine_want: Muốn biết vì sao không cần bridge khi agent tự kéo việc.
spine_want_lines: ["claude:0faf0bb2#L657"]
spine_obstacle: "Gateway OpenClaw chỉ nghe trên máy cục bộ, Cloudflare không gọi tới được."
spine_obstacle_lines: ["claude:0faf0bb2#L707"]
spine_turn: Tưởng bridge chỉ còn là tuỳ chọn vì agent tự kéo việc; hoá ra mỗi heartbeat là một lượt LLM khi HEARTBEAT.md không rỗng.
spine_turn_lines: ["claude:0faf0bb2#L659", "claude:0faf0bb2#L707"]
spine_action: "Đọc mã heartbeat-runner, sửa lesson agent-bridge và đề xuất một waker không dùng LLM."
spine_action_lines: ["claude:0faf0bb2#L671", "claude:0faf0bb2#L690"]
spine_outcome: "Bridge vẫn cần, chỉ là bản đơn giản; 5 agent mỗi 5 phút là khoảng 1.440 lượt LLM mỗi ngày."
spine_outcome_lines: ["claude:0faf0bb2#L707"]
spine_takeaway: Đo chi phí một vòng kiểm tra định kỳ bằng số lượt model mỗi ngày trước khi chọn kiểu pull.
spine_takeaway_lines: ["claude:0faf0bb2#L707"]
completeness: 7
---

# Heartbeat của OpenClaw tốn một lượt LLM mỗi nhịp: 'bridge chỉ còn tuỳ chọn' là nói quá

**Góc kể:** Bộ dựng công ty một người chạy bằng đội agent AI đang chọn cách agent nhận việc. Người làm tin rằng bridge chỉ còn là tuỳ chọn vì agent tự kéo việc, nhưng heartbeat của OpenClaw tốn một lượt LLM mỗi nhịp khi file kiểm tra không rỗng: 5 agent mỗi 5 phút là khoảng 1.440 lượt mỗi ngày. Ai chọn kiểu pull cho agent nên đo chi phí vòng kiểm tra trước khi bỏ bridge.
**Bối cảnh:** Mình đã nói bridge không còn cần vì agent tự kéo việc từ hàng đợi; chủ hỏi 'tại sao không cần cái này'.
**Chuyện gì xảy ra:** heartbeat-runner chỉ bỏ qua lượt khi HEARTBEAT.md rỗng. Nếu agent phải kiểm tra inbox thì mỗi nhịp là một lần gọi model: 5 agent mỗi 5 phút là khoảng 1.440 lượt mỗi ngày, gần như toàn bộ trả lời 'không có việc'. Mình sửa lesson và đề xuất một waker không dùng LLM, chỉ gọi openclaw agent khi có việc.
**Bài học:** Trước khi chọn kiểu pull, đo chi phí của một vòng kiểm tra định kỳ bằng số lượt model mỗi ngày.
**Artefact:** Bảng số lượt mỗi ngày theo số agent và chu kỳ.
