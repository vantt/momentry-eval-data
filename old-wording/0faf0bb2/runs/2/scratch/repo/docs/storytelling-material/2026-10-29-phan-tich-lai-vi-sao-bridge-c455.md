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
hook: "Chỉ để hỏi 'không có việc', 5 agent đốt 1.440 lượt LLM mỗi ngày"
tension: nho_ma_to
sides: ["Bridge tưởng chỉ là tuỳ chọn, heartbeat 60 phút là đủ", "1.440 lượt LLM mỗi ngày chỉ để trả lời 'không có việc', phản hồi chậm 60 phút"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Phân tích lại vì sao 'bridge chỉ là tuỳ chọn' là sai: heartbeat 60 phút và chi phí một lượt LLM mỗi lần kiểm tra

**Bối cảnh:** Câu hỏi của chủ: vì sao không cần bridge. Lúc đầu agent đã trả lời 'bridge chỉ còn là tuỳ chọn'.
**Chuyện gì xảy ra:** Kiểm tra heartbeat-runner.ts cho thấy OpenClaw chỉ bỏ qua lượt heartbeat khi HEARTBEAT.md rỗng. Nếu 5 agent kiểm tra inbox mỗi 5 phút sẽ tốn khoảng 1.440 lượt LLM mỗi ngày chỉ để trả lời 'không có việc', và phản hồi chậm tới 60 phút. Sau đó phải sửa lại: vẫn cần bridge, chỉ là bridge rất đơn giản, không dùng LLM.
**Bài học:** Kiểm tra chi phí của một lần 'thức dậy' trước khi chọn kiến trúc poll; một lượt LLM trả lời 'không' vẫn tốn tiền.
**Artefact:** Sơ đồ bridge ba tầng (waker không dùng LLM, heartbeat thưa, gateway) dạng ASCII.
