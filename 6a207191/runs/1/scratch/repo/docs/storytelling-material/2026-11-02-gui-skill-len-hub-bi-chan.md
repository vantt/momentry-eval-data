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
hook: "Gửi skill lên hub bị chặn ba lần, lỗi gợi ý cờ không tồn tại"
tension: khac
sides: ["Thông báo lỗi chỉ cách sửa bằng cờ --user", "Cờ đó không tồn tại, vì máy 0.8.0 còn hub đã 0.12.0"]
strength: 2
stakes: 2
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
**Góc người ngoài:** cách làm phổ biến là Dev thường thêm `--force` hoặc chạy lại với quyền cao hơn khi gặp lỗi chặn. Với AI agent, nhiều người cho phép tất cả mọi thứ để khỏi bị hỏi; ở đây khác ở Công cụ chủ ý chặn `--yes` cho hub chưa tin cậy để agent không đem token đi gửi bừa. Agent tôn trọng ranh giới đó, và việc nó kiểm chứng khẳng định của người dùng bằng cách grep các file cấu hình thật cho thấy một mẫu làm việc an toàn mà người đọc muốn có.
