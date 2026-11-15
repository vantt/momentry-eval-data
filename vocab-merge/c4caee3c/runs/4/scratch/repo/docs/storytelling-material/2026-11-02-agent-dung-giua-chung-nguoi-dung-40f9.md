---
id: 2026-11-02-agent-dung-giua-chung-nguoi-dung-40f9
code: M-0GQQ
aliases: [M-0GQQ]
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L3442", "claude:c4caee3c#L3452", "claude:c4caee3c#L3504", "claude:c4caee3c#L3510"]
hook: "Agent dừng giữa chừng, mỗi lượt CI mất 10 đến 20 phút"
tension: gap_ma_phai_chon
sides: ["đợi báo cáo cuối của agent", "commit ngay 34 test xanh vì chờ CI quá lâu"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent dừng giữa chừng, người dùng phải gọi lại; mỗi lượt CI 10 đến 20 phút

**Bối cảnh:** Agent review upstream dừng mà không báo. Chạy lại phải dựng bốn cây OHS từ đầu.
**Chuyện gì xảy ra:** Lead phát hiện không có tiến trình nào đang chạy và báo cáo vẫn là bản cũ, rồi gọi agent tiếp tục. Người dùng than là chậm. Lead commit phần mã đã xong (34 test xanh) mà không đợi báo cáo cuối. Mỗi lần sửa lỗi CI tốn 10 đến 20 phút chờ.
**Bài học:** Kiểm tiến trình thật thay vì tin trạng thái của agent; tách phần commit được khỏi phần chờ tính toán dài.
