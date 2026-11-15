---
id: 2026-10-29-nhan-nham-rang-bridge-la-tuy-c455
code: M-GZA4
aliases: [M-GZA4]
date: 2026-10-29
repo: repo
status: raw
signals: [dao_quyet_dinh]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:0faf0bb2#L657", "claude:0faf0bb2#L660", "claude:0faf0bb2#L667", "claude:0faf0bb2#L671", "claude:0faf0bb2#L686", "claude:0faf0bb2#L707"]
hook: "5 agent kiểm tra inbox mỗi 5 phút đốt 1.440 lượt LLM mỗi ngày"
tension: nho_ma_to
sides: ["Một dòng chỉ dẫn kiểm tra inbox trong HEARTBEAT.md", "Mỗi lượt là một lần gọi model, gần hết để trả lời 'không có việc'"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "fgOPC là bộ dựng công ty một người vận hành bằng AI agent, và người làm muốn agent tự kéo việc từ hàng đợi thay vì có bridge đẩy việc tới. Ban đầu tưởng bridge có thể bỏ, vì agent tự kéo được. Hoá ra trên OpenClaw mỗi lần heartbeat là một lượt gọi model, dù không có việc: 5 agent kiểm tra mỗi 5 phút đã là khoảng 1.440 lượt mỗi ngày. Bridge vẫn cần, nhưng chỉ là một script không dùng LLM. Ai thiết kế agent tự chạy nền nên biết vòng kiểm tra việc có tốn token hay không."
audience: dev xây hệ agent tự chạy nền
spine_context: "fgOPC là bộ dựng công ty một người vận hành bằng AI agent. Người làm muốn agent tự kéo việc từ hàng đợi trên Cloudflare D1, không cần server Node chạy thường trực."
spine_context_lines: [profile, "claude:0faf0bb2#L493"]
spine_want: "Có một schema chuẩn cho các thực thể để sinh API/MCP, để agent kết nối trực tiếp và bỏ bridge đẩy việc."
spine_want_lines: ["claude:0faf0bb2#L493"]
spine_obstacle: "Gateway OpenClaw chỉ nghe localhost nên Cloudflare không gọi tới được. Mỗi lần heartbeat là một lượt gọi model, dù không có việc."
spine_obstacle_lines: ["claude:0faf0bb2#L707"]
spine_turn: "Tưởng bridge chỉ còn là tuỳ chọn vì agent tự kéo việc. Hoá ra mỗi heartbeat tốn một lượt LLM, nên vòng kiểm tra inbox qua LLM là lãng phí."
spine_turn_lines: ["claude:0faf0bb2#L657", "claude:0faf0bb2#L707"]
spine_action: "Đọc mã heartbeat của OpenClaw: chỉ bỏ qua lượt khi HEARTBEAT.md rỗng. Sửa lại kết luận: bridge vẫn cần, nhưng là script không dùng LLM."
spine_action_lines: ["claude:0faf0bb2#L672", "claude:0faf0bb2#L707"]
spine_outcome: Đã sửa câu trả lời. Người dùng hỏi tiếp có dùng Paperclip luôn được không; câu trả lời là gần đúng nhưng phải thử tương thích trước.
spine_outcome_lines: ["claude:0faf0bb2#L712", "claude:0faf0bb2#L716"]
spine_takeaway: "Vòng kiểm tra việc của agent không nên đi qua LLM. Giữ nó ở một tiến trình rẻ, heartbeat chỉ là lưới an toàn."
spine_takeaway_lines: ["claude:0faf0bb2#L707"]
completeness: 7
---

# Nhận nhầm rằng bridge là tuỳ chọn: mỗi heartbeat của agent tốn một lượt LLM

**Góc kể:** fgOPC là bộ dựng công ty một người vận hành bằng AI agent, và người làm muốn agent tự kéo việc từ hàng đợi thay vì có bridge đẩy việc tới. Ban đầu tưởng bridge có thể bỏ, vì agent tự kéo được. Hoá ra trên OpenClaw mỗi lần heartbeat là một lượt gọi model, dù không có việc: 5 agent kiểm tra mỗi 5 phút đã là khoảng 1.440 lượt mỗi ngày. Bridge vẫn cần, nhưng chỉ là một script không dùng LLM. Ai thiết kế agent tự chạy nền nên biết vòng kiểm tra việc có tốn token hay không.
**Bối cảnh:** Đã nói bridge chỉ còn là tuỳ chọn vì agent tự kéo việc từ hàng đợi. Người dùng hỏi lại.
**Chuyện gì xảy ra:** Đọc mã heartbeat cho thấy OpenClaw chỉ bỏ qua lượt khi HEARTBEAT.md rỗng. Nếu có chỉ dẫn kiểm tra inbox thì mỗi lượt là một lần gọi model. Ví dụ 5 agent mỗi 5 phút tạo khoảng 1.440 lượt mỗi ngày, gần như toàn bộ để trả lời 'không có việc'. Đã sửa lại: bridge vẫn cần, nhưng chỉ là một script không dùng LLM, hỏi định kỳ.
**Bài học:** Đừng để vòng kiểm tra việc của agent đi qua LLM. Giữ nó ở một tiến trình không tốn token, còn heartbeat chỉ là lưới an toàn.
**Artefact:** Bảng tính số lượt mỗi ngày theo số agent và chu kỳ kiểm tra.
