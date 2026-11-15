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
hook: "Một lệnh pandoc đổi ghi chú thành docx cho khách dùng Word"
tension: none
sides: []
strength: 0
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "Một nhóm đang làm nghiên cứu churn cho một phòng nha khoa, chuẩn bị bản tổng hợp và outline cho buổi báo cáo điều hành."
spine_context_lines: ["claude:5a1e7c02#L1"]
spine_want: Muốn chọn ba phát hiện cho buổi báo cáo 20 phút thứ Năm.
spine_want_lines: ["claude:5a1e7c02#L52"]
spine_obstacle: Có chín phát hiện nhưng chỉ đủ chỗ cho ba.
spine_obstacle_lines: ["claude:5a1e7c02#L52"]
spine_action: Chuyển ghi chú markdown thành bảng trích dẫn bốn cột và xuất outline sang docx bằng pandoc.
spine_action_lines: ["claude:5a1e7c02#L61", "claude:5a1e7c02#L63"]
spine_outcome: Bảng trích dẫn có 29 câu trích; outline.docx đã được tạo.
spine_outcome_lines: ["claude:5a1e7c02#L65"]
completeness: 5
---

# Từ ghi chú thô tới bảng trích dẫn và docx cho khách dùng Word

**Bối cảnh:** Khách hàng dùng Word, nên mọi sản phẩm cuối phải là docx. Ghi chú gốc viết bằng markdown.
**Chuyện gì xảy ra:** Một script Python chuyển ghi chú markdown thành bảng trích dẫn 4 cột (trích dẫn, người, phòng khám, chủ đề) với 29 trích dẫn trong 31 dòng, gồm tiêu đề và dòng phân cách. Pandoc xuất outline sang docx chỉ bằng một lệnh. Quy trình giữ markdown làm nguồn và chỉ xuất docx ở bước cuối.
**Bài học:** Giữ nguồn là markdown, xuất docx ở bước cuối, và đưa cột nguồn vào bảng trích dẫn để truy ngược được từng câu về bản ghi gốc.
**Artefact:** Ảnh bảng quote bank trong Word, với tên người và tên phòng khám đã được thay bằng mã.
