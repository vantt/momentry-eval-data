---
id: 2026-11-02-sua-loi-tuong-tac-bo-sua
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L1470", "claude:c4caee3c#L1478", "claude:c4caee3c#L1480"]
hook: "Bộ sửa gõ sai biến 'phone' thành từ khác, từ đồng nghĩa tụt hạng"
tension: giup_ma_hai
sides: ["Bộ sửa gõ sai nhằm giúp tìm đúng hơn", "Nó viết lại từ đồng nghĩa, thứ hạng tụt từ 4 xuống 7"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Sửa lỗi tương tác: bộ sửa gõ sai làm từ đồng nghĩa tụt thứ hạng

**Bối cảnh:** Sau khi gộp nhánh sửa gõ sai (V17) với nhánh từ đồng nghĩa (V18), vi-synonym rớt.
**Chuyện gì xảy ra:** Bộ sửa gõ sai viết lại từ như phone thành một từ gần nghĩa trong vault, nên từ đồng nghĩa không còn được nhận dạng. Thứ hạng của một câu tụt từ 4 xuống 7, và Hit@5 vi-synonym tụt xuống 0,73. Sửa đổi: lexicon khớp cả dạng người dùng gõ lẫn dạng đã sửa, và từ người dùng viết theo dạng đồng nghĩa được coi là từ đã biết.
**Bài học:** Khi hai bộ xử lý truy vấn chồng lên nhau, bộ nào chạy trước có thể che mất tín hiệu của bộ sau.
**Artefact:** Ví dụ một cặp từ đồng nghĩa, không kèm câu hỏi thật.
