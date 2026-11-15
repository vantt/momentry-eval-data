---
id: 2026-10-21-file-huong-dan-agent-vuot-tran-fd46
code: M-70Y9
aliases: [M-70Y9]
date: 2026-10-21
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, số trước sau]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L262", "claude:9514b261#L902"]
hook: "File hướng dẫn agent dài 46.754 byte, Codex cắt im lặng ở 32 KiB"
tension: nho_ma_to
sides: ["file hướng dẫn viết đầy đủ cho agent", "vượt trần 1,4 lần, phần thừa bị cắt không báo"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# File hướng dẫn agent vượt trần 32 KiB của Codex, và Codex cắt im lặng

**Bối cảnh:** Repo có một file hướng dẫn agent dùng chung cho nhiều CLI. Codex chỉ đọc 32 KiB đầu.
**Chuyện gì xảy ra:** File đo 46.754 byte, sau đó 46.919 byte, vượt trần khoảng 1,4 lần. Codex cắt sau trần mà không báo. Vì khối AgentKit chưa commit, agent không git add nguyên file mà chỉ stage phần của mình.
**Bài học:** Đo byte file hướng dẫn theo trần của từng CLI và coi trần là ràng buộc thiết kế, không chỉ là lưu ý.
**Artefact:** Biểu đồ kích thước file so với vạch 32 KiB.
