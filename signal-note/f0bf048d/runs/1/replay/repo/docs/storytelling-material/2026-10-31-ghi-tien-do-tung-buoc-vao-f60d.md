---
id: 2026-10-31-ghi-tien-do-tung-buoc-vao-f60d
code: M-XZB7
aliases: [M-XZB7]
date: 2026-10-31
repo: repo
status: raw
signals: []
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:f0bf048d#L2385", "claude:f0bf048d#L2394", "claude:f0bf048d#L2562", "claude:f0bf048d#L2578"]
hook: "Đổi người hay hết phiên, không ai biết đã làm đến đâu"
tension: nho_ma_to
sides: ["trạng thái chỉ nằm trong chat", "hết phiên là mất, không ai biết tiến độ"]
strength: 1
stakes: 0
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Ghi tiến độ từng bước vào một file trong repo (có mục trạng thái: đã làm, đang làm, hoãn, còn lại), thay vì chỉ báo trong chat. Cập nhật file này trước mỗi lần commit.

**Chuyện gì xảy ra:** Ghi tiến độ từng bước vào một file trong repo (có mục trạng thái: đã làm, đang làm, hoãn, còn lại), thay vì chỉ báo trong chat. Cập nhật file này trước mỗi lần commit.
**Góc người ngoài:** cách làm phổ biến là Phần lớn người dùng chỉ để trạng thái trong cuộc trò chuyện với AI, nên khi phiên kết thúc hoặc đổi người, không ai biết đã làm đến đâu; ở đây khác ở Trạng thái nằm trong repo, người khác hoặc phiên sau đọc được ngay. Người đọc sẽ muốn biết cách giữ một file tiến độ như vậy mà không tốn công.
