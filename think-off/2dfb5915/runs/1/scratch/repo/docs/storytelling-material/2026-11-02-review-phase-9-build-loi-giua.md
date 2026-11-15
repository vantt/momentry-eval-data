---
id: 2026-11-02-review-phase-9-build-loi-giua
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1038", "claude:2dfb5915#L1046", "claude:2dfb5915#L1094"]
hook: "Build index lỗi một lần, edges cũ ở lại mãi"
tension: nho_ma_to
sides: ["một lần build lỗi giữa chừng", "edges cũ tồn tại mãi, index sai vĩnh viễn"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Review phase 9: build lỗi giữa chừng làm index sai mãi

**Bối cảnh:** Index SQLite ghi ba transaction riêng. Adapter lỗi giữa chừng khiến note đã lưu nhưng edges cũ không được tính lại.
**Chuyện gì xảy ra:** Reviewer tìm ra hai lỗi mức cao: build lỗi làm edges cũ tồn tại mãi, và hai build chạy cùng lúc gây lỗi lock. Sửa bằng cờ dirty trong meta, file lock cạnh DB, và đọc note trước khi mở transaction ghi. Python có cùng lỗi edges cũ, nên bản Rust ghi nhận đây là khác biệt có chủ đích cho phần lock.
**Bài học:** Thao tác build index phải đáng tin: đánh dấu dirty trước khi ghi và xoá dấu khi xong.
**Artefact:** Sơ đồ ba transaction trước và sau khi sửa.
