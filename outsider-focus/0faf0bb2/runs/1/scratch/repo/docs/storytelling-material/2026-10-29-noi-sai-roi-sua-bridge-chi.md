---
id: 2026-10-29-noi-sai-roi-sua-bridge-chi
date: 2026-10-29
repo: repo
status: raw
signals: [đảo quyết định]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:0faf0bb2#L657", "claude:0faf0bb2#L679", "claude:0faf0bb2#L690", "claude:0faf0bb2#L707"]
hook: "Nói 'bridge chỉ là tuỳ chọn' sai: heartbeat tốn 1.440 lượt gọi model mỗi ngày"
tension: tuong_ma_hoa_ra
sides: ["Tưởng heartbeat thay được bridge", "Gần 1.440 lượt model mỗi ngày chỉ để trả lời 'không có việc'"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Nói sai rồi sửa: 'bridge chỉ còn là tuỳ chọn' hoá ra là sai

**Bối cảnh:** Sau khi quyết định agent tự kéo việc từ D1, mình nói bridge chỉ còn là tuỳ chọn. Người dùng hỏi vì sao, mình kiểm tra lại code heartbeat của OpenClaw.
**Chuyện gì xảy ra:** Heartbeat chỉ được bỏ qua khi file HEARTBEAT.md rỗng. Để agent tự kiểm inbox, mỗi lần heartbeat là một lượt gọi model, với 5 agent và chu kỳ 5 phút là khoảng 1.440 lượt mỗi ngày, gần như toàn bộ để trả lời 'không có việc'. Heartbeat mặc định 60 phút nên phản hồi cũng chậm. Mình sửa lại: cần một bridge không dùng LLM, hỏi định kỳ, và heartbeat chỉ là lưới an toàn.
**Bài học:** Trước khi khẳng định hệ thống 'không cần' một thành phần, tìm trong code điều kiện thực tế của nó. Một lượt heartbeat rỗng vẫn có thể là một lượt gọi model.
**Artefact:** Sơ đồ opc-waker: vòng hỏi 15–30 giây, không có việc thì 0 token.
**Góc người ngoài:** cách làm phổ biến là Dev thường tin README, bài blog hoặc câu trả lời của AI. Nếu có thử thì thử bằng demo, ít khi grep source để xem công cụ thật sự hành xử ra sao; ở đây khác ở Người đọc muốn biết cách biến AI từ 'nói nghe hợp lý' thành 'có dẫn chứng file:dòng', và cách ghi đính chính để quyết định chọn công cụ không dựa trên suy đoán. Nhiều kết luận trong phiên bị đảo ngược nhờ bước này.
