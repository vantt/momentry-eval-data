---
id: 2026-11-02-goi-p01-bi-phat-hien-thieu-40f9
code: M-XVTQ
aliases: [M-XVTQ]
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L1570", "claude:c4caee3c#L1715"]
hook: "Gói P01 xong rồi mới thiếu năm điểm, vá thêm mà hai gói cũ vẫn chạy"
tension: it_ma_nhieu
sides: ["Gói thiếu năm điểm sau khi làm xong", "Hợp đồng chỉ thêm, hai gói cũ không cần sửa dòng nào"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Gói P01 bị phát hiện thiếu năm điểm sau khi làm xong, vá thêm không phá gói cũ

**Bối cảnh:** Gói tiếng Việt cần thêm khả năng mà hợp đồng P01 chưa có.
**Chuyện gì xảy ra:** Năm chỗ thiếu gồm khớp chính xác và khớp cụm, trọng số view theo câu tìm, matchedTerms cho rescore, ngữ cảnh trong signature, và cận trên cho lệnh dò tiền tố. Hợp đồng vẫn apiVersion 1 và chỉ thêm, nên hai gói cũ không cần sửa.
**Bài học:** Viết hợp đồng plug-in từ test của người dùng gói, không từ suy đoán; nếu phải thêm thì chỉ thêm, không đổi.
