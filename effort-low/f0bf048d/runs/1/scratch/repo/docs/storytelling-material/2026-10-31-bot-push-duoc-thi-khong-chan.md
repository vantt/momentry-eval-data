---
id: 2026-10-31-bot-push-duoc-thi-khong-chan
date: 2026-10-31
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, đảo quyết định có lý do]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L2367", "claude:f0bf048d#L2373", "claude:f0bf048d#L3327", "claude:f0bf048d#L3340", "claude:f0bf048d#L3345"]
hook: "Muốn bot chỉ đọc, nhưng repo private cá nhân không cấp được quyền đó"
tension: cam_ma_van_lot
sides: ["Dặn bot không push, đề xuất tài khoản chỉ đọc", "GitHub không cho chỉ đọc nên bot vẫn push được, phải đổi sang deploy key"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Bot push được thì không chặn được bằng lời dặn: chọn đường không có quyền ghi

**Bối cảnh:** Agent cần push cấu hình lên repo private trên GitHub gói Free, nhưng repo cũng chứa script chạy bằng sudo.
**Chuyện gì xảy ra:** Phiên này đã đề xuất tài khoản chỉ đọc cho bot, nhưng GitHub cho biết repo private cá nhân không cấp được quyền chỉ đọc, nên đề xuất phải rút lại. Cách thay: bot chỉ có deploy key đọc, còn người duyệt fetch nhánh ops/* về xem diff rồi merge. Phương án Pro (khoảng 4 USD) được giữ làm lựa chọn sau.
**Bài học:** Nếu một hệ thống tự động có thể lên git bằng quyền ghi, nó có thể ghi vào nhánh chính; giới hạn bằng cách không cấp quyền ghi, đừng dựa vào hook hay lời dặn.
**Artefact:** Sơ đồ luồng: agent commit nhánh ops/* → người fetch, xem diff, merge. Che tên repo nếu cần.
