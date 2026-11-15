---
id: 2026-11-03-quarantine-release-all-tha-hang-cho-d5ef
code: M-ZNX7
aliases: [M-ZNX7]
date: 2026-11-03
repo: repo
status: raw
signals: [nguoi_duyet_may_soan]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L3315", "claude:ab9a1dd8#L3333", "claude:ab9a1dd8#L3366", "claude:ab9a1dd8#L3397"]
hook: "Thả hàng chờ cả loạt, nhưng chuyện vi phạm vẫn bị giữ"
tension: cam_ma_van_lot
sides: ["Lệnh --release all thả mọi thứ", "Mỗi chuyện được kiểm lại, chuyện vi phạm vẫn nằm lại"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Quarantine --release all: thả hàng chờ nhưng kiểm lại từng chuyện

**Bối cảnh:** Người dùng yêu cầu thêm lệnh thả hàng chờ quarantine cho tất cả chuyện.
**Chuyện gì xảy ra:** Agent đọc code quarantine trước, rồi thêm `--release all`. Mỗi chuyện được kiểm lại trước khi thả, nên chuyện còn vi phạm vẫn bị giữ. Test chuyển từ 234 lên 235 và tài liệu lệnh được sinh lại.
**Bài học:** Thả hàng loạt phải kiểm lại từng mục, không tin trạng thái cũ.
**Artefact:** Đầu ra lệnh --release all trên hai chuyện mẫu (một sạch, một còn vi phạm). Che nội dung chuyện.
