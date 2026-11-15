---
id: 2026-10-29-bo-bridge-roi-phai-nhan-lai-c455
code: M-E042
aliases: [M-E042]
date: 2026-10-29
repo: repo
status: raw
signals: [đảo quyết định có lý do, số trước sau]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L657", "claude:0faf0bb2#L660", "claude:0faf0bb2#L667", "claude:0faf0bb2#L671", "claude:0faf0bb2#L707"]
hook: "Bỏ bridge vì 'chỉ là tuỳ chọn', rồi 1.440 lượt LLM mỗi ngày chỉ để nói 'không có việc'"
tension: giup_ma_hai
sides: ["Bỏ bridge cho gọn", "5 agent tốn 1.440 lượt LLM/ngày cho 'không có việc'"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Bỏ bridge rồi phải nhận lại: mỗi heartbeat của OpenClaw tốn một lượt LLM

**Bối cảnh:** Sau khi chọn Paperclip với kiến trúc không server, agent đề xuất để agent tự kéo việc và coi bridge chỉ là tuỳ chọn.
**Chuyện gì xảy ra:** Agent khẳng định 'bridge chỉ còn là tuỳ chọn'. Người dùng hỏi lại, agent kiểm tra heartbeat-runner và thấy OpenClaw chỉ bỏ qua lượt khi HEARTBEAT.md rỗng. Nếu agent kiểm tra inbox qua heartbeat, 5 agent mỗi 5 phút sẽ tốn khoảng 1.440 lượt LLM mỗi ngày, gần như chỉ để trả lời 'không có việc'. Kết luận đảo ngược: cần một bridge không dùng LLM, poll mỗi 15–30 giây.
**Bài học:** Trước khi chọn pull hay push, hãy đếm chi phí của mỗi lần 'thức dậy' khi không có việc.
**Artefact:** Sơ đồ ba khối: waker không dùng LLM, gateway, heartbeat thưa.
