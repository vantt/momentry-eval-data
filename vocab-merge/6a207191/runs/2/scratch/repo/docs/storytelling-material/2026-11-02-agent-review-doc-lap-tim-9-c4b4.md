---
id: 2026-11-02-agent-review-doc-lap-tim-9-c4b4
code: M-086C
aliases: [M-086C]
date: 2026-11-02
repo: repo
status: raw
signals: [người duyệt máy soạn, nguyên nhân bất ngờ]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:6a207191#L673", "claude:6a207191#L681", "claude:6a207191#L690", "claude:6a207191#L937"]
hook: "Skill mẫu về chuẩn viết tool lại vi phạm chính quy tắc của nó: 9 lỗi"
tension: tuong_ma_hoa_ra
sides: ["Skill dạy cách viết CLI đúng chuẩn", "Reviewer tìm ra 9 lỗi, kể cả vi phạm chính quy tắc"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent review độc lập tìm 9 lỗi, trong đó skill mẫu vi phạm chính quy tắc của nó

**Bối cảnh:** Khi skill có 230 rule, người dùng nhờ một agent mức suy nghĩ cao review như thể nó là người sắp dùng skill để làm packaging cho một Go CLI có MCP server.
**Chuyện gì xảy ra:** Reviewer đóng vai một agent được giao việc thật, đi theo đúng quy trình trong skill và chạy thử script. Nó tìm ra ba nhóm lỗi: lệnh bị mâu thuẫn (một file dùng setup, file khác bỏ setup), installer mẫu thiếu --help và xóa cài đặt mà không hỏi, và nguyên tắc 'proven ways first' lại trỏ Go CLI sang code Rust. Lỗi nặng nhất là chuỗi lệnh dành cho agent không bao giờ chạy connect, nên agent chỉ đọc --help sẽ không đăng ký được MCP server. Sau đó agent sửa 9 điểm và thêm bước Verify 12 mục vào SKILL.md.
**Bài học:** Cho reviewer đóng vai người dùng thật và đi theo quy trình của tài liệu; lỗi thường nằm ở chỗ tài liệu tự mâu thuẫn, không nằm ở từng dòng.
**Artefact:** Bảng 9 finding được xếp hạng must-fix và nên sửa. Không có nội dung riêng tư.
