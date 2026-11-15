---
id: 2026-11-03-codex-khong-chay-hook-momentry-tu
date: 2026-11-03
repo: repo
status: raw
signals: ["2"]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L3192", "claude:ab9a1dd8#L3195", "claude:ab9a1dd8#L3206", "claude:ab9a1dd8#L3228", "claude:ab9a1dd8#L3306"]
hook: "Codex lặng lẽ bỏ qua hook momentry từ đầu vì hai tên sự kiện sai"
tension: cam_ma_van_lot
sides: ["hook đã cài, CI vẫn xanh", "Codex bỏ qua im lặng vì tên sự kiện sai kiểu"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Codex không chạy hook momentry từ đầu: tên sự kiện viết sai kiểu bị bỏ qua

**Bối cảnh:** momentry ghi tên sự kiện kiểu snake_case cho Codex, trong khi hooks.json của Codex cần tên dạng PascalCase.
**Chuyện gì xảy ra:** Codex bỏ qua hook không báo lỗi nên không ai biết trong thời gian dài. Khi đối chiếu với mã nguồn Codex, agent thấy hai tên sai. Đổi thành PreCompact, SessionEnd và SessionStart, thêm SessionEnd, rồi push; CI vẫn xanh.
**Bài học:** Đối chiếu tên sự kiện với schema thật của host thay vì đoán, vì hook bị bỏ qua không để lại dấu vết.
**Artefact:** Bảng so sánh tên sự kiện trước và sau khi sửa.
