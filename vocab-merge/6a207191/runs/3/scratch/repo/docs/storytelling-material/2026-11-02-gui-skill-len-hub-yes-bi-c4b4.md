---
id: 2026-11-02-gui-skill-len-hub-yes-bi-c4b4
code: M-DHRT
aliases: [M-DHRT]
date: 2026-11-02
repo: repo
status: raw
signals: [ràng buộc thiết kế, nguyên nhân bất ngờ]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:6a207191#L996", "claude:6a207191#L1004", "claude:6a207191#L1068", "claude:6a207191#L1074", "claude:6a207191#L1085", "claude:6a207191#L1102", "claude:6a207191#L1297", "claude:6a207191#L1315"]
hook: "Gửi skill lên hub: cờ --yes bị chặn, gợi ý lại sai cờ"
tension: giup_ma_hai
sides: ["Lệnh báo lỗi gợi ý cờ để sửa", "Cờ --user được gợi ý lại không hề tồn tại"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Gửi skill lên hub: --yes bị chặn, lệnh ! không hỏi được, và gợi ý sai cờ

**Bối cảnh:** Skill đã hoàn chỉnh và agent muốn gửi lên hub skillstation chạy trên máy khác, để người duyệt bên đó xử lý.
**Chuyện gì xảy ra:** Lần gửi đầu bị từ chối khi dùng --yes vì hub chưa được tin cậy ở cấp user: token và file sẽ đi ra ngoài máy. Khi lệnh chạy qua khung ! của Claude Code, nó không có terminal tương tác nên chỉ in bản xem trước và chưa gửi gì. Lệnh tin cậy hub gợi ý cờ --user không tồn tại. CLI lúc đó là 0.8.0 còn hub là 0.12.0; sau khi cập nhật lên 0.13.0 thì lệnh kết nối có --global và gửi được bằng --yes.
**Bài học:** Thông báo lỗi phải kèm một lệnh copy chạy được; gợi ý một cờ không tồn tại khiến người dùng mất thêm một vòng.
**Artefact:** Khối thông báo lỗi WHY và FIX. Cần che đường dẫn file token và địa chỉ hub.
