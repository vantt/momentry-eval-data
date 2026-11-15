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
hook: "11 agent cùng một repo, có agent dừng mà không báo"
tension: khac
sides: ["11 agent chạy song song cùng một repo", "Có agent im lặng dừng, lead phải nhắn mới chạy tiếp"]
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
**Góc người ngoài:** cách làm phổ biến là Mở nhiều tab/phiên AI cùng một thư mục, hoặc giao từng việc lẻ bằng prompt miệng, trạng thái nằm trong đầu người hoặc trong ngữ cảnh chat; ở đây khác ở Cách tổ chức giống một đội: brief chung, vùng file cho phép, đầu ra có cấu trúc, sổ trạng thái ngoài ngữ cảnh. Nhờ đó 11 agent chạy song song và việc điều phối còn tiếp tục được sau khi ngữ cảnh bị nén. Người đọc dùng AI hằng ngày muốn mẫu này.
