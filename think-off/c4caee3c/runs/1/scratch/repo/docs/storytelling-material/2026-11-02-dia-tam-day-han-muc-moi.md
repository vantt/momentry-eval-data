---
id: 2026-11-02-dia-tam-day-han-muc-moi
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L492", "claude:c4caee3c#L508", "claude:c4caee3c#L610", "claude:c4caee3c#L618", "claude:c4caee3c#L632", "claude:c4caee3c#L740"]
hook: "Đĩa tạm đầy hạn mức, 11 agent hỏng shell cùng lúc, không mất việc nào"
tension: nho_ma_to
sides: ["Một thư mục tạm chạm hạn mức", "Mọi lệnh shell của 11 agent đều hỏng"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đĩa tạm đầy hạn mức, mọi lệnh shell của mọi agent đều hỏng

**Bối cảnh:** Mỗi agent làm việc trong một worktree riêng, và mỗi worktree cài node_modules khoảng 1,3 GB. Các worktree lại nằm trong /tmp, một tmpfs 16 GB có hạn mức.
**Chuyện gì xảy ra:** Ghi file trạng thái bị lỗi EDQUOT, rồi cả lệnh tìm dung lượng cũng lỗi exit 134. Lead dừng toàn bộ 11 agent, chuyển các worktree sang ổ đĩa thật, sửa đường dẫn bằng git worktree repair và cho agent chạy lại. Không mất phần việc nào; /tmp về còn 26%.
**Bài học:** Đặt worktree và cache phụ thuộc trên ổ có dung lượng lớn; tmpfs có hạn mức sẽ làm hỏng cả hệ thống công cụ chứ không riêng việc đang làm.
**Artefact:** Dòng df trước và sau khi chuyển worktree. Không chụp đường dẫn riêng.
