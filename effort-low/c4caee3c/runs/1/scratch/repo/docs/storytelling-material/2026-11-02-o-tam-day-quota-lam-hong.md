---
id: 2026-11-02-o-tam-day-quota-lam-hong
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, số trước sau]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:c4caee3c#L492", "claude:c4caee3c#L506", "claude:c4caee3c#L508", "claude:c4caee3c#L611", "claude:c4caee3c#L621", "claude:c4caee3c#L740", "claude:c4caee3c#L3972"]
hook: "Ổ tạm đầy 16 GB, mọi agent hỏng cùng lúc, kể cả lệnh chẩn đoán"
tension: nho_ma_to
sides: ["Mỗi worktree chỉ tốn khoảng 1,3 GB node_modules", "Đầy hạn mức thì mọi lệnh của mọi agent đều lỗi, cả lệnh chẩn đoán"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Ổ tạm đầy quota làm hỏng mọi agent cùng lúc

**Bối cảnh:** Điều phối 11 agent song song, mỗi worktree kéo theo thư mục phụ thuộc lớn, và tất cả đặt trong /tmp là tmpfs có hạn mức.
**Chuyện gì xảy ra:** Mỗi worktree tốn khoảng 1,3 GB node_modules. Khi hạn mức 16 GB đầy, mọi lệnh shell của mọi agent đều lỗi với EDQUOT, kể cả lệnh để chẩn đoán. Cách xử lý là dừng hết agent, chuyển nguyên worktree sang ổ thật và cho git nhận lại đường dẫn bằng worktree repair, không xoá gì. Sau đó /tmp còn 26 %, còn thư mục làm việc tạm giảm từ 21 GB xuống 6,4 GB sau khi dọn phần việc đã xong.
**Bài học:** Đặt worktree, build và log lớn ngoài tmpfs ngay từ đầu; lỗi quota làm mọi agent chết cùng lúc, không chỉ agent đang ghi.
**Artefact:** Bảng dung lượng /tmp trước và sau khi chuyển worktree. Che đường dẫn thư mục người dùng.
**Góc người ngoài:** cách làm phổ biến là Thường để tích lũy đến khi đầy đĩa mới dọn, hoặc xoá hết một lượt; ở đây khác ở Phiên này giảm từ 21G xuống 6,4G mà vẫn giữ các thứ còn dùng, sau khi ổ tạm từng đầy quota làm hỏng mọi agent. Người đọc muốn biết cách không rơi vào tình huống đó.
