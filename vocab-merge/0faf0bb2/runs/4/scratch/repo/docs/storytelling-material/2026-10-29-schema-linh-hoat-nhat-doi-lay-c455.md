---
id: 2026-10-29-schema-linh-hoat-nhat-doi-lay-c455
code: M-MV24
aliases: [M-MV24]
date: 2026-10-29
repo: repo
status: raw
signals: [điều đánh đổi]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L3335", "claude:0faf0bb2#L3365"]
hook: "Schema càng linh hoạt càng mất luật cứng, nên ràng buộc phải ở server"
tension: chon_mot_mat_mot
sides: ["Linh hoạt tối đa: tạo object ngay lúc chạy như Twenty", "Mất các luật cứng, phải giữ ràng buộc ở server"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Schema linh hoạt nhất đổi lấy việc mất luật cứng; CRM linh hoạt nhất, quản lý dự án thì Multica

**Bối cảnh:** Người dùng muốn thêm field, trạng thái và loại thực thể mới mà không cần sửa code.
**Chuyện gì xảy ra:** Có ba mức linh hoạt: field tuỳ chỉnh, trạng thái hoặc quy trình, và loại thực thể mới. Chỉ Twenty, một CRM khoảng 60k sao dùng AGPL, tạo được object lúc runtime và sinh schema GraphQL từ metadata. Trong nhóm quản lý dự án, Multica có custom field theo workspace với 7 kiểu, lưu trong JSONB nên đổi tên không cần migrate. Linh hoạt quá sẽ mất luật cứng, nên các ràng buộc cần nằm ở server.
**Bài học:** Schema linh hoạt đổi lấy việc mất luật cứng. Giữ luật chuyển trạng thái trong code, không đưa vào metadata.
**Artefact:** Bảng ba mức linh hoạt của các hệ thống.
