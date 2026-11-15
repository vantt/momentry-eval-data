---
id: 2026-10-29-don-paperclip-xoa-khoang-2-4-c455
code: M-6R07
aliases: [M-6R07]
date: 2026-10-29
repo: repo
status: raw
signals: [so_truoc_so_sau, rang_buoc_thiet_ke]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L2414", "claude:0faf0bb2#L2452", "claude:0faf0bb2#L2460", "claude:0faf0bb2#L2469", "claude:0faf0bb2#L2481", "claude:0faf0bb2#L2483", "claude:0faf0bb2#L2504", "claude:0faf0bb2#L2556", "claude:0faf0bb2#L2572", "claude:0faf0bb2#L2624"]
hook: "Một lệnh gỡ cài đặt giữ lại dữ liệu, nhưng 2,4 GB vẫn bị xoá"
tension: chon_mot_mat_mot
sides: ["Gỡ CLI thì giữ được dữ liệu", "Xoá sạch 2,4 GB, hai session không khôi phục được"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Dọn Paperclip: xoá khoảng 2,4 GB và toàn bộ dữ liệu công ty mẫu, không khôi phục được

**Bối cảnh:** Chủ yêu cầu dọn sạch Paperclip sau spike, trong khi AICoworker vẫn đang dùng.
**Chuyện gì xảy ra:** Gỡ CLI bằng paperclipai uninstall (giữ lại dữ liệu), rồi xoá ~/.paperclip gồm instance và database, khoảng 2,4 GB. Sau đó xoá thêm cache npx, 6 file capture và 2 transcript đã vào thùng rác, khiến hai session này không khôi phục được. Runbook §10 có bảng hoàn tác để dựng lại trong khoảng 15 phút.
**Bài học:** Trước khi xoá dữ liệu thử, liệt kê rõ sẽ mất gì và khôi phục bằng cách nào, rồi mới xoá.
**Artefact:** Bảng 'đã gỡ / còn giữ' trong runbook.
