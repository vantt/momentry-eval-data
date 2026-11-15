---
id: 2026-10-29-heartbeat-ton-mot-luot-llm-moi
date: 2026-10-29
repo: repo
status: raw
signals: [đảo quyết định có lý do, số trước/sau]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L660", "claude:0faf0bb2#L667", "claude:0faf0bb2#L671", "claude:0faf0bb2#L686", "claude:0faf0bb2#L707"]
hook: "5 agent hỏi 'có việc không?' mỗi 5 phút: 1.440 lượt model mỗi ngày để nghe 'không'"
tension: nho_ma_to
sides: ["Heartbeat chỉ là một cái ping nhỏ", "Mỗi lần tốn một lượt LLM, khoảng 1.440 lượt/ngày chỉ để trả lời 'không có việc'"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Heartbeat tốn một lượt LLM mỗi lần, trừ khi HEARTBEAT.md rỗng: bridge từ 'tuỳ chọn' thành bắt buộc

**Bối cảnh:** Kiến trúc đề xuất ban đầu cho rằng agent tự kéo việc từ D1 thì không cần bridge.
**Chuyện gì xảy ra:** Đọc heartbeat-runner cho thấy OpenClaw chỉ bỏ qua lượt heartbeat khi HEARTBEAT.md rỗng. Nếu agent phải kiểm tra inbox định kỳ, mỗi lần heartbeat là một lượt gọi model. Ước tính 5 agent, mỗi 5 phút, khoảng 1.440 lượt mỗi ngày gần như chỉ để trả lời 'không có việc'. Vì vậy phát biểu 'bridge chỉ còn là tuỳ chọn' bị sửa thành bridge là bắt buộc nhưng rất đơn giản.
**Bài học:** Khi thiết kế cơ chế đánh thức agent, đếm số lượt gọi model khi không có việc, không chỉ số lượt khi có việc.
**Artefact:** Phép tính 5 agent × 288 lần/ngày = 1.440 lượt, dạng bảng nhỏ.
