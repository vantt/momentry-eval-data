---
id: 2026-11-02-dieu-phoi-song-song-11-agent
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:c4caee3c#L87", "claude:c4caee3c#L92", "claude:c4caee3c#L97", "claude:c4caee3c#L153", "claude:c4caee3c#L162", "claude:c4caee3c#L1199", "claude:c4caee3c#L1221", "claude:c4caee3c#L3452"]
hook: "11 agent sửa chung một repo mà cây làm việc vẫn sạch"
tension: khac
sides: ["11 agent cùng làm trên một repo", "cây chung vẫn sạch nhờ xuất bản vá riêng rồi ghép"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Điều phối song song: 11 agent cùng một repo, giữ cây chung sạch

**Bối cảnh:** Kế hoạch chia việc thành các task V00 đến V25. Mỗi agent làm trên worktree riêng và lead ghép nhánh theo phụ thuộc.
**Chuyện gì xảy ra:** Agent con xuất bản vá vào thư mục chung, lead ghép theo thứ tự phụ thuộc. Có agent dừng mà không báo lại, lead phải gửi tin để tiếp tục. Trạng thái được ghi ra file để còn dùng sau khi nén ngữ cảnh. Sau khi ghép xong, lead dọn worktree.
**Bài học:** Tách worktree cho từng agent, xếp hàng ghép theo phụ thuộc, và ghi trạng thái ra file bền vững.
**Artefact:** Sơ đồ phụ thuộc giữa các task.
**Góc người ngoài:** cách làm phổ biến là Phần lớn người làm một mình sẽ dừng công việc, sửa xong rồi chạy lại từ đầu, hoặc không bao giờ có nhiều tiến trình song song để phải điều phối; ở đây khác ở Một tiến trình điều phối giữ được trạng thái và nhận chỉ đạo mới qua tin nhắn, không mất ngữ cảnh; người đọc sẽ hỏi làm sao để tiến trình dài không bị mất đà.
