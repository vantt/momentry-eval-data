---
id: 2026-10-14-tu-ghi-chu-tho-toi-bang-8a83
code: M-XN6V
aliases: [M-XN6V]
date: 2026-10-14
repo: repo
status: raw
signals: [artefact_nhin_duoc, rang_buoc_thiet_ke]
source: "chat Claude, claude:5a1e7c02"
sessions: ["claude:5a1e7c02"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:5a1e7c02#L60", "claude:5a1e7c02#L61", "claude:5a1e7c02#L62", "claude:5a1e7c02#L63", "claude:5a1e7c02#L64", "claude:5a1e7c02#L65"]
hook: "Giữ markdown làm gốc, Pandoc đổi sang Word chỉ bằng một lệnh"
tension: it_ma_nhieu
sides: ["Một lệnh Pandoc và một script Python nhỏ", "Bảng 29 trích dẫn và file docx cho khách dùng Word"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Từ ghi chú thô tới bảng trích dẫn và docx cho khách dùng Word

**Bối cảnh:** Khách hàng dùng Word, nên mọi sản phẩm cuối phải là docx. Ghi chú gốc viết bằng markdown.
**Chuyện gì xảy ra:** Một script Python chuyển ghi chú markdown thành bảng trích dẫn 4 cột (trích dẫn, người, phòng khám, chủ đề) với 29 trích dẫn trong 31 dòng, gồm tiêu đề và dòng phân cách. Pandoc xuất outline sang docx chỉ bằng một lệnh. Quy trình giữ markdown làm nguồn và chỉ xuất docx ở bước cuối.
**Bài học:** Giữ nguồn là markdown, xuất docx ở bước cuối, và đưa cột nguồn vào bảng trích dẫn để truy ngược được từng câu về bản ghi gốc.
**Artefact:** Ảnh bảng quote bank trong Word, với tên người và tên phòng khám đã được thay bằng mã.
