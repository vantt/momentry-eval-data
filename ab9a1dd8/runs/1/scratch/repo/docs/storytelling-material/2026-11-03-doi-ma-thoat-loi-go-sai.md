---
id: 2026-11-03-doi-ma-thoat-loi-go-sai
date: 2026-11-03
repo: repo
status: raw
signals: [đảo quyết định, ràng buộc]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:ab9a1dd8#L264", "claude:ab9a1dd8#L300", "claude:ab9a1dd8#L616", "claude:ab9a1dd8#L735", "claude:ab9a1dd8#L889"]
hook: "Đổi mã thoát cho chuẩn, script cũ sẽ bỏ lọt vi phạm"
tension: giup_ma_hai
sides: ["Đổi mã thoát cho đúng chuẩn", "Script chỉ kiểm mã 2 bỏ lọt vi phạm riêng tư"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đổi mã thoát: lỗi gõ sai thành lỗi có kết quả

**Bối cảnh:** Mã thoát đã được công bố trong README và PRD. Skill muốn 1 là lỗi chung và 2 là sai cú pháp.
**Chuyện gì xảy ra:** Bảng cũ: 1 là gõ sai lệnh, 2 là check thấy vi phạm riêng tư. Agent đề xuất giữ bảng cũ vì script pre-commit có thể đợi mã 2 để chặn commit. User chọn chuẩn. Đổi kéo theo sửa nhiều test và mục Breaking trong CHANGELOG. Ai viết script chỉ kiểm mã 2 sẽ bỏ lọt vi phạm nếu không cập nhật.
**Bài học:** Đổi mã thoát là đổi hợp đồng công khai; sai ở chỗ kiểm riêng tư là lỗi im lặng nguy hiểm nhất.
**Artefact:** Bảng mã thoát trước và sau trong CHANGELOG.
