---
id: 2026-11-02-het-dung-luong-tmp-giua-luc
date: 2026-11-02
repo: repo
status: raw
signals: [Nguyên nhân bất ngờ, Ràng buộc định hình thiết kế]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:c4caee3c#L492", "claude:c4caee3c#L506", "claude:c4caee3c#L508", "claude:c4caee3c#L612", "claude:c4caee3c#L632", "claude:c4caee3c#L740"]
hook: "11 agent đang chạy thì /tmp đầy, mọi lệnh shell hỏng"
tension: nho_ma_to
sides: ["Chỉ đặt worktree nhầm chỗ", "Cả 11 agent mất shell cùng lúc"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hết dung lượng /tmp giữa lúc 11 agent đang chạy: worktree đặt nhầm chỗ

**Bối cảnh:** Mỗi worktree có node_modules khoảng 1,3G, đặt trong tmpfs /tmp có hạn mức 16G.
**Chuyện gì xảy ra:** Ghi file trạng thái báo EDQUOT, lệnh shell của mọi agent hỏng. Chuyển toàn bộ worktree sang /home/.../ohs-wt, git worktree repair, gửi SendMessage cho 11 agent tiếp tục. Không mất phần việc dở; /tmp về 26%.
**Bài học:** Đặt worktree và build lớn ngoài /tmp; ghi vào brief chung để mọi agent biết.
**Artefact:** Không cần.
**Góc người ngoài:** cách làm phổ biến là Thường người dùng xoá bừa thư mục tạm, hoặc chạy lại từ đầu làm mất công việc đang dở; ở đây khác ở Không mất phần việc dang dở nào: worktree được di chuyển có kiểm, mỗi agent được báo đường dẫn mới và tiếp tục, và dọn dẹp sau đó chỉ xoá những gì đã có bằng chứng là xong (đã merge, đã đọc artifact). Người đọc muốn có quy trình tương tự khi đĩa đầy.
