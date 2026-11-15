---
id: 2026-11-03-doc-ma-nguon-codex-de-hieu
date: 2026-11-03
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L3106", "claude:ab9a1dd8#L3117", "claude:ab9a1dd8#L3139", "claude:ab9a1dd8#L3149", "claude:ab9a1dd8#L3157"]
hook: "Khỏi tự tính hash phức tạp: Codex có sẵn cờ bypass_hook_trust"
tension: it_ma_nhieu
sides: ["công thức hash phức tạp, dễ sai", "một cờ bypass_hook_trust có sẵn trong mã nguồn"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đọc mã nguồn Codex để hiểu cơ chế duyệt tin cậy hook

**Bối cảnh:** Codex yêu cầu duyệt tin cậy từng hook qua trusted_hash sha256 trong config.toml, và không có tài liệu nói cách tính hash.
**Chuyện gì xảy ra:** Agent tìm trong mã nguồn mở và thấy công thức hash phức tạp, nhiều chỗ dễ sai khi tự tính. Thay vào đó, agent tìm thấy cờ bypass_hook_trust, dùng cho môi trường probe.
**Bài học:** Khi host đòi xác thực bằng hash, đọc mã nguồn mở để biết cách tính hoặc tìm cờ được hỗ trợ, đừng tự suy công thức.
**Artefact:** Đoạn config.toml với trusted_hash và cờ, che giá trị hash.
