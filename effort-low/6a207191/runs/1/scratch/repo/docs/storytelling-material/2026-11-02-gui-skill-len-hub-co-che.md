---
id: 2026-11-02-gui-skill-len-hub-co-che
date: 2026-11-02
repo: repo
status: raw
signals: [ràng buộc thiết kế, nguyên nhân bất ngờ, khác]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:6a207191#L996", "claude:6a207191#L1007", "claude:6a207191#L1066", "claude:6a207191#L1068", "claude:6a207191#L1074", "claude:6a207191#L1086", "claude:6a207191#L1094", "claude:6a207191#L1102", "claude:6a207191#L1109", "claude:6a207191#L1168"]
hook: "Lỗi bảo dùng cờ --user, nhưng CLI chẳng có cờ nào như thế"
tension: cam_ma_van_lot
sides: ["Thông báo lỗi chỉ đường bằng cờ --user", "CLI không hề có cờ --user"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Gửi skill lên hub: cơ chế chặn --yes và cờ gợi ý không tồn tại

**Bối cảnh:** Skill nội bộ được gửi lên một hub chạy trên máy khác qua CLI skillstation, để người duyệt bên đó xem xét.
**Chuyện gì xảy ra:** Lệnh --yes bị chặn vì hub chưa được tin cậy ở cấp user, nên token không được gửi. Lệnh chạy qua prefix ! trong Claude Code không phải terminal tương tác, nên chỉ in bản xem trước và không gửi gì. Thông báo lỗi gợi ý cờ --user, nhưng CLI không có cờ đó. CLI trên máy này là 0.8.0 trong khi hub là 0.12.0. Sau khi nâng lên 0.13.0 và kết nối toàn cục, việc gửi mới thành công.
**Bài học:** Cơ chế không tự gửi token là đúng. Nhưng thông báo lỗi phải là một lệnh dán chạy được, và lệch phiên bản giữa client và hub là nguồn lỗi chính.
**Artefact:** Đoạn thông báo lỗi và bản xem trước. Che địa chỉ hub và đường dẫn token.
**Góc người ngoài:** cách làm phổ biến là Người làm thường thử thêm cờ như --force, --yes hoặc sửa quyền cho qua, rồi mới hỏi; ở đây khác ở Coi cơ chế chặn là thông tin về môi trường, không phải trở ngại cần vượt. Người đọc sẽ hỏi: làm sao để agent nhận ra một chặn là có chủ ý?.
