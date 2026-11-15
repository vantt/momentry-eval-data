---
id: 2026-11-03-doc-schema-transcript-that-ma-khong-d5ef
code: M-C044
aliases: [M-C044]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:ab9a1dd8#L3501", "claude:ab9a1dd8#L3502", "claude:ab9a1dd8#L3507", "claude:ab9a1dd8#L3520", "claude:ab9a1dd8#L3528", "claude:ab9a1dd8#L3605", "claude:ab9a1dd8#L3606"]
hook: "Đọc cấu trúc transcript thật mà không in nội dung nào"
tension: none
sides: []
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đọc schema transcript thật mà không in nội dung: chỉ in khoá và kiểu

**Bối cảnh:** Viết bộ đọc pi, omp, agy cần schema thật, trong khi transcript chứa nội dung riêng.
**Chuyện gì xảy ra:** Agent viết script in cấu trúc bản ghi JSONL: kiểu, vai trò, khoá, không in giá trị. Lệnh glob cho omp lỗi, phải dùng find với -size để lấy phiên lớn hơn 20 KB. Bộ đọc agy chạy đúng trên 5 transcript thật.
**Bài học:** Khi phải nhìn dữ liệu có riêng tư, in cấu trúc thay vì giá trị, và viết script đó trước khi đọc.
**Artefact:** Output cấu trúc bản ghi (khoá và kiểu, không giá trị).
**Góc người ngoài:** cách làm phổ biến là Dev thường mở file mẫu xem luôn nội dung để viết parser, hoặc chạy công cụ bên thứ ba thẳng với mạng bật; ở đây khác ở Agent giữ quyền riêng tư của transcript và không gửi yêu cầu ra ngoài khi thử, bằng cách chỉ in khoá/kiểu và chặn mạng. Người đọc sẽ hỏi làm sao vừa có schema đúng vừa không lộ dữ liệu.
