---
id: 2026-11-02-gui-skill-len-hub-bi-chan
date: 2026-11-02
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, khác]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:6a207191#L990", "claude:6a207191#L996", "claude:6a207191#L1004", "claude:6a207191#L1007", "claude:6a207191#L1066", "claude:6a207191#L1074", "claude:6a207191#L1085", "claude:6a207191#L1102", "claude:6a207191#L1112", "claude:6a207191#L1152", "claude:6a207191#L1168"]
hook: "Gửi skill bị chặn ba lần, vì lệnh cũ gợi ý một cờ không tồn tại"
tension: giup_ma_hai
sides: ["thông báo lỗi gợi ý cờ --user", "cờ đó không tồn tại, do máy 0.8.0 và hub 0.12.0 lệch bản"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Gửi skill lên hub bị chặn ba lần: --yes không được phép, cờ gợi ý không tồn tại, máy hub lệch phiên bản

**Bối cảnh:** Mục tiêu là đưa skill lên hub riêng để các máy khác dùng qua skill_resolve. Skillstation trên máy này cũ hơn bản trên hub.
**Chuyện gì xảy ra:** Lần gửi đầu bị từ chối vì hub chưa được tin cậy ở cấp user, nên --yes không được phép gửi token. Lệnh chạy qua prefix '!' trong Claude Code không tương tác, nên chỉ in bản xem trước gồm 29 file (70,5 KB) và không gửi gì. Thông báo lỗi gợi ý cờ --user không tồn tại, đây là lỗi của bản cũ (máy 0.8.0, hub 0.12.0). Sau khi cập nhật và người dùng chạy connect --global, doctor báo Healthy và lần gửi thành công.
**Bài học:** Lệnh xác nhận không chạy được ở chế độ không tương tác. Gợi ý trong thông báo lỗi phải là một lệnh dán vào chạy được, nếu không cả người lẫn agent đều mất thời gian.
**Artefact:** Hai đoạn lỗi: 'unknown argument' và 'action_required'. Che địa chỉ hub và token.
**Góc người ngoài:** cách làm phổ biến là Nhiều agent chạy thẳng các lệnh ghi vào cấu hình người dùng, hoặc tự tìm cờ ép qua chặn bảo mật; ở đây khác ở Với lệnh như kết nối hub cho mọi dự án, agent dừng lại và để người dùng xác nhận, đồng thời giải thích hậu quả. Người đọc muốn có cách giữ quyền quyết định trong khi vẫn để agent làm phần còn lại.
