---
id: 2026-11-02-sau-khi-user-sua-mot-quyet
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:2dfb5915#L1715", "claude:2dfb5915#L2308", "claude:2dfb5915#L2358", "claude:2dfb5915#L3662", "claude:2dfb5915#L3921"]
hook: "User đổi ý giữa chừng, agent không làm lại mà ghi vào DECISIONS"
tension: none
sides: []
strength: 0
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Sau khi user sửa một quyết định ngay trong lúc làm, agent không làm lại việc đã xong mà ghi quyết định vào tài liệu chung (DECISIONS, plan, handoff) và cập nhật các nơi bị ảnh hưởng.

**Chuyện gì xảy ra:** Sau khi user sửa một quyết định ngay trong lúc làm, agent không làm lại việc đã xong mà ghi quyết định vào tài liệu chung (DECISIONS, plan, handoff) và cập nhật các nơi bị ảnh hưởng.
**Góc người ngoài:** cách làm phổ biến là Thường người làm sẽ sửa code mà quên sửa tài liệu, hoặc phải nhắc đi nhắc lại; ở đây khác ở Người đọc sẽ hỏi làm sao nhiều tài liệu đồng bộ được: phiên này ghi quyết định có ngày và lý do, cập nhật phiên bản pin, và báo lại cho agent khác đang chạy.
