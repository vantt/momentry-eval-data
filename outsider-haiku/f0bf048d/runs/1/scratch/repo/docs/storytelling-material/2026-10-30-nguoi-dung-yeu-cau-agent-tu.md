---
id: 2026-10-30-nguoi-dung-yeu-cau-agent-tu
date: 2026-10-30
repo: repo
status: raw
signals: []
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:f0bf048d#L920", "claude:f0bf048d#L923", "claude:f0bf048d#L929", "claude:f0bf048d#L2478", "claude:f0bf048d#L2487", "claude:f0bf048d#L2501", "claude:f0bf048d#L3181", "claude:f0bf048d#L3193"]
hook: "Bảo agent tự làm, nó giao việc mà không dám gợi ý đáp án"
tension: khac
sides: ["AI quen làm xong thay người dùng", "agent nhường việc và giấu lỗi đã thấy để thử agent khác"]
strength: 2
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Người dùng yêu cầu agent 'tự làm', không phải làm thay. Agent chuyển sang vai trò giao việc: viết issue chỉ nêu mục tiêu, không kể trước lỗi đã thấy, rồi theo dõi kết quả để kiểm tra agent có tự phát hiện được không. Sau đó nó tự tạo agent thử và issue thử nghiệm, đọc số liệu chạy và comment để xác nhận.

**Chuyện gì xảy ra:** Người dùng yêu cầu agent 'tự làm', không phải làm thay. Agent chuyển sang vai trò giao việc: viết issue chỉ nêu mục tiêu, không kể trước lỗi đã thấy, rồi theo dõi kết quả để kiểm tra agent có tự phát hiện được không. Sau đó nó tự tạo agent thử và issue thử nghiệm, đọc số liệu chạy và comment để xác nhận.
**Góc người ngoài:** cách làm phổ biến là AI thường làm xong việc cho người dùng, và giao việc cho agent khác có thể bị gợi ý sẵn câu trả lời; ở đây khác ở Agent kiểm thử bằng cách đóng vai người giao việc thật, nên kết quả phản ánh năng lực của agent đích. Người đọc muốn biết cách thiết kế bài kiểm tra như vậy cho agent của mình.
