---
id: 2026-11-02-merge-xong-moi-thay-hong-typo-40f9
code: M-06ZE
aliases: [M-06ZE]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, so_truoc_so_sau]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L1352", "claude:c4caee3c#L1368", "claude:c4caee3c#L1424", "claude:c4caee3c#L1434", "claude:c4caee3c#L1445", "claude:c4caee3c#L1458", "claude:c4caee3c#L1470", "claude:c4caee3c#L1478"]
hook: "Merge xong mới thấy sửa lỗi gõ làm hỏng từ điển đồng nghĩa"
tension: giup_ma_hai
sides: ["Bộ sửa lỗi gõ sai ra đời để tìm đúng hơn", "Nó ghi đè từ điển, đồng nghĩa tụt 0,80 xuống 0,73"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Merge xong mới thấy hỏng: typo sửa nhầm từ điển đồng nghĩa

**Bối cảnh:** Ba nhánh cùng sửa một module truy vấn. Mỗi nhánh được agent riêng làm và đo riêng.
**Chuyện gì xảy ra:** Sau khi merge nhánh gõ sai, bộ sửa lỗi gõ sai ghi đè các từ đã có trong từ điển trước khi từ điển kịp xử lý. Hit@5 của hạng mục đồng nghĩa giảm từ 0,80 xuống 0,73. Merge nhánh từ điển bị hủy vì xung đột ở bốn file, và việc giải xung đột được giao lại cho chính agent đó. Sau khi sửa, hạng mục trở lại 0,80 và nDCG@5 tổng lên 0,909.
**Bài học:** Số đo trước khi merge không phải số thật. Đo lại trên nhánh đã merge, và kiểm xem một bước mới có ghi đè bước cũ không.
**Artefact:** Bảng so sánh điểm trước và sau merge theo hạng mục (không chứa câu hỏi).
