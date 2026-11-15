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
hook: "Giữ markdown làm gốc, một lệnh Pandoc ra file Word cho khách"
tension: none
sides: []
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "Một người làm nghiên cứu về việc khách rời bỏ (churn) cho chuỗi phòng khám nha khoa, dựa trên 14 cuộc phỏng vấn và dữ liệu khảo sát."
spine_context_lines: ["claude:5a1e7c02#L1"]
spine_want: Cần bản nháp tổng hợp và dàn ý cho buổi trình bày điều hành thứ Năm.
spine_want_lines: ["claude:5a1e7c02#L1"]
spine_obstacle: "Chỉ có 20 phút với ba người nghe, trong khi có chín phát hiện phải chọn ra ba."
spine_obstacle_lines: ["claude:5a1e7c02#L52"]
spine_action: "Chuyển bảng trích dẫn sang bảng 4 cột (trích dẫn, người, phòng khám, chủ đề) và xuất dàn ý sang docx cho khách dùng Word."
spine_action_lines: ["claude:5a1e7c02#L60", "claude:5a1e7c02#L61", "claude:5a1e7c02#L63"]
spine_outcome: Bảng trích dẫn có 29 câu và file docx đã sẵn sàng.
spine_outcome_lines: ["claude:5a1e7c02#L64", "claude:5a1e7c02#L65"]
completeness: 5
---

# Từ ghi chú thô tới bảng trích dẫn và docx cho khách dùng Word

**Bối cảnh:** Khách hàng dùng Word, nên mọi sản phẩm cuối phải là docx. Ghi chú gốc viết bằng markdown.
**Chuyện gì xảy ra:** Một script Python chuyển ghi chú markdown thành bảng trích dẫn 4 cột (trích dẫn, người, phòng khám, chủ đề) với 29 trích dẫn trong 31 dòng, gồm tiêu đề và dòng phân cách. Pandoc xuất outline sang docx chỉ bằng một lệnh. Quy trình giữ markdown làm nguồn và chỉ xuất docx ở bước cuối.
**Bài học:** Giữ nguồn là markdown, xuất docx ở bước cuối, và đưa cột nguồn vào bảng trích dẫn để truy ngược được từng câu về bản ghi gốc.
**Artefact:** Ảnh bảng quote bank trong Word, với tên người và tên phòng khám đã được thay bằng mã.
