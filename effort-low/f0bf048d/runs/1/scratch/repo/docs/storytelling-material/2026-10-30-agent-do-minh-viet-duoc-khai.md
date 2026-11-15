---
id: 2026-10-30-agent-do-minh-viet-duoc-khai
date: 2026-10-30
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, ràng buộc định hình thiết kế]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L915", "claude:f0bf048d#L1122", "claude:f0bf048d#L1125"]
hook: "Agent tôi viết ra ghi đè luôn team Coding đang chạy, gỡ 3 agent"
tension: giup_ma_hai
sides: ["Deploy đầu tiên để dựng team Marketing", "Ghi đè team Coding về bản cũ, gỡ 3 agent khỏi squad"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent do mình viết được khai báo sai workspace và ghi đè đội khác

**Bối cảnh:** Gói marketing và gói coding của hai phiên khác nhau cùng deploy vào một workspace Multica.
**Chuyện gì xảy ra:** Lần deploy đầu tiên của phiên này ghi đè team Coding (Khoa, Minh, Quân) về bản cũ, gỡ 3 agent khỏi squad và gắn sai workflow. Lý do: gói opc-studio còn giữ bản Coding cũ, và bỏ qua các dòng ngoài phần Marketing khi đọc plan. Khôi phục bằng deploy lại gói coding từ file của phiên kia, plan về 0 thay đổi.
**Bài học:** Deploy không xoá thực thể, nhưng ghi đè cấu hình. Plan toàn bộ diff trước khi deploy, đừng chỉ đọc phần của mình, và mỗi gói chỉ giữ phần thuộc về nó.
**Artefact:** Đoạn log plan báo '+/~ agent' trước và sau khi khôi phục; che tên workspace nếu cần.
