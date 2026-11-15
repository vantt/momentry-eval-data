---
id: 2026-11-02-han-muc-tmp-day-moi-agent-40f9
code: M-4R9E
aliases: [M-4R9E]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, rang_buoc_thiet_ke]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:c4caee3c#L492", "claude:c4caee3c#L506", "claude:c4caee3c#L507", "claude:c4caee3c#L508", "claude:c4caee3c#L621", "claude:c4caee3c#L680", "claude:c4caee3c#L720"]
hook: "/tmp đầy làm mọi agent hỏng lệnh, kể cả lệnh kiểm dung lượng"
tension: nho_ma_to
sides: ["Một ổ tạm đầy hạn mức", "Mọi agent hỏng shell cùng lúc, lệnh kiểm tra cũng hỏng"]
strength: 3
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hạn mức /tmp đầy, mọi agent hỏng lệnh shell cùng lúc

**Bối cảnh:** Điều phối 11 agent song song. Mỗi worktree kéo theo node_modules khoảng 1,3 GB, mà toàn bộ worktree lại nằm trong /tmp, một tmpfs 16 GB có hạn mức.
**Chuyện gì xảy ra:** Một lệnh ghi báo EDQUOT. Lệnh kiểm tra dung lượng cũng hỏng vì không ghi được file đầu ra của chính nó. Lead dừng hết agent, chuyển các worktree sang ổ chính, chạy git worktree repair cho từng cái rồi gửi lệnh tiếp tục cho từng agent. Không mất việc dở nào, và /tmp giảm từ đầy xuống 26%.
**Bài học:** Hạn mức đĩa dùng chung là điểm nghẽn ẩn. Đặt worktree và node_modules trên ổ có dung lượng thật, đừng đặt trong tmpfs.
**Artefact:** Bảng df trước và sau khi chuyển, cùng dòng lỗi EDQUOT. Che đường dẫn thư mục người dùng.
**Góc người ngoài:** cách làm phổ biến là Khi hết quota, người ta thường xoá bớt file hoặc dọn cache, không di chuyển cả cây đang dở rồi sửa lại liên kết worktree; ở đây khác ở Đây là cách cứu công việc đang chạy dở khi hạ tầng hỏng, không cần làm lại từ đầu. Người đọc muốn biết cách repair worktree và nhắn lại cho agent đang dừng.
