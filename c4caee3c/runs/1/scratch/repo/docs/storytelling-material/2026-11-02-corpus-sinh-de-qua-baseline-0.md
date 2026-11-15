---
id: 2026-11-02-corpus-sinh-de-qua-baseline-0
date: 2026-11-02
repo: repo
status: raw
signals: ["Số trước, số sau", Đảo quyết định có lý do]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:c4caee3c#L315", "claude:c4caee3c#L334", "claude:c4caee3c#L1034", "claude:c4caee3c#L1044"]
hook: "Baseline 0,93 vì corpus quá dễ: mục tiêu không thể đo được"
tension: tuong_ma_hoa_ra
sides: ["Baseline 0,93 trông như đã rất tốt", "Corpus dễ, làm khó lại thì chỉ còn 0,27"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Corpus sinh dễ quá: baseline 0,93 khiến mục tiêu G3 không thể đạt

**Bối cảnh:** Bộ eval tiếng Việt tự sinh có mục tiêu G3: Hit@5 từ 0,85 trở lên và gấp đôi baseline. Baseline upstream đã đạt 0,93 ở hạng mục vi-unaccented, nên điều kiện gấp đôi là không thể.
**Chuyện gì xảy ra:** Agent tìm ra nguyên nhân: SQLite unicode61 chỉ bỏ dấu được âm tiết có một dấu, không bỏ được âm tiết có hai dấu và chữ đ. Truy vấn trùng tiêu đề note nên nhánh tiêu đề và nhánh vector cứu baseline. Người duyệt chọn làm corpus khó hơn, không hạ ngưỡng. Sau đó baseline vi-unaccented giảm còn 0,27 và vi-dd còn 0,40.
**Bài học:** Khi baseline đã chạm trần, kiểm tra corpus có đo đúng thứ cần đo trước khi hạ ngưỡng.
**Artefact:** Bảng Hit@5 theo hạng mục trước và sau khi làm khó corpus. Che tên note và câu truy vấn.
**Góc người ngoài:** cách làm phổ biến là Tự viết vài chục câu test bằng tay hoặc sinh ngẫu nhiên bằng LLM rồi đo; nếu điểm baseline đã cao thì coi như hệ thống tốt; ở đây khác ở Corpus phải đủ khó để baseline thấp (0,27) thì mới đo được cải thiện; phát hiện được nhờ nhận ra tiêu đề trùng câu hỏi làm lộ đáp án. Người đọc làm search/RAG sẽ hỏi cách kiểm tra bộ eval có thật sự phân biệt được tốt/xấu.
