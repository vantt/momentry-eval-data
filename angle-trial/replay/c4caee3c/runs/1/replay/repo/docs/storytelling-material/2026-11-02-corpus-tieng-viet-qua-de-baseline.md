---
id: 2026-11-02-corpus-tieng-viet-qua-de-baseline
date: 2026-11-02
repo: repo
status: raw
signals: [số trước sau, đảo quyết định có lý do]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L315", "claude:c4caee3c#L1044", "claude:c4caee3c#L1150", "claude:c4caee3c#L1264"]
hook: "Baseline 0,93 tưởng tốt, thật ra bộ test quá dễ để đo gì"
tension: tuong_ma_hoa_ra
sides: ["Điểm 0,93 trông như hệ thống tìm tốt", "Tiêu đề trùng câu hỏi nên không đo được gì; làm khó thì còn 0,27"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Bộ test tiếng Việt cho kết quả Hit@5 0,93 nên trông tìm kiếm đã tốt. Thật ra mỗi câu tìm đều là tiêu đề của chính ghi chú đó, nên hệ thống tìm được nhờ tiêu đề chứ không nhờ bộ tìm kiếm xử lý được dấu. Khi làm corpus khó hơn, điểm giảm còn 0,27 với chữ không dấu và 0,40 với chữ đ. Benchmark có đáp án lộ ra ngoài sẽ che mất lỗi tìm kiếm, nên cần đo lại với nhiều kiểu gõ."
audience: dev làm tìm kiếm hoặc đo chất lượng tìm kiếm cho ứng dụng tiếng Việt
---

# Corpus tiếng Việt quá dễ: baseline 0,93 không đo được gì

**Góc kể:** Bộ test tiếng Việt cho kết quả Hit@5 0,93 nên trông tìm kiếm đã tốt. Thật ra mỗi câu tìm đều là tiêu đề của chính ghi chú đó, nên hệ thống tìm được nhờ tiêu đề chứ không nhờ bộ tìm kiếm xử lý được dấu. Khi làm corpus khó hơn, điểm giảm còn 0,27 với chữ không dấu và 0,40 với chữ đ. Benchmark có đáp án lộ ra ngoài sẽ che mất lỗi tìm kiếm, nên cần đo lại với nhiều kiểu gõ.
**Bối cảnh:** Mục tiêu G3 yêu cầu Hit@5 từ 0,85 và gấp đôi baseline. Baseline upstream đã đạt 0,93 trên corpus sinh nên điều kiện gấp đôi không thể đạt.
**Chuyện gì xảy ra:** Chẩn đoán: tiêu đề note trùng đúng cụm câu tìm, nên nhánh tiêu đề và nhánh vector tìm ra note dù FTS5 không bỏ được dấu. Đo unicode61 trực tiếp: chỉ bỏ được syllable có một dấu, không bỏ được syllable hai dấu hay chữ đ. Người dùng chọn làm corpus khó hơn thay vì hạ ngưỡng. Hit@5 không dấu từ 0,93 xuống 0,27, dd từ 0,87 xuống 0,40. Gói tiếng Việt sau đó đưa không dấu lên 1,00.
**Bài học:** Benchmark có tiêu đề lộ câu tìm sẽ che mất lỗi tìm; đo lại với các kiểu gõ khác và đúng tokenizer của hệ thống.
**Artefact:** Bảng Hit@5 trước và sau theo hạng mục.
