---
id: 2026-11-03-codex-bo-qua-hook-cua-momentry
date: 2026-11-03
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L3192", "claude:ab9a1dd8#L3195", "claude:ab9a1dd8#L3206", "claude:ab9a1dd8#L3229"]
hook: "Codex bỏ qua hook của tôi từ đầu vì sai tên sự kiện"
tension: nho_ma_to
sides: ["sai tên sự kiện (pre_compact thay PreCompact)", "Codex bỏ qua hook mà không báo gì"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Codex bỏ qua hook của momentry suốt từ đầu vì sai tên sự kiện

**Bối cảnh:** Hook Codex được viết theo tên sự kiện kiểu snake_case. Test của momentry vẫn pass vì chỉ khớp với chuỗi tự viết.
**Chuyện gì xảy ra:** Codex đòi PreCompact, SessionEnd và SessionStart. momentry ghi pre_compact và session_start, nên Codex bỏ qua mà không báo gì. Lỗi nằm ở chỗ không ai nghi: test chỉ kiểm chuỗi nội bộ, không kiểm host thật. Sửa xong thì thêm cả SessionEnd.
**Bài học:** Test khớp chuỗi tự viết chứng minh rất ít; muốn biết host đọc tên gì thì phải thử bằng host thật.
**Artefact:** Bảng so sánh tên sự kiện của Claude và Codex.
