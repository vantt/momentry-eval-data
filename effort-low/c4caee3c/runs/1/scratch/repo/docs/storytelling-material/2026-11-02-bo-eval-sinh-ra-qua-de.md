---
id: 2026-11-02-bo-eval-sinh-ra-qua-de
date: 2026-11-02
repo: repo
status: raw
signals: [số trước sau, nguyên nhân bất ngờ]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:c4caee3c#L1044", "claude:c4caee3c#L1150", "claude:c4caee3c#L1264"]
hook: "Bộ eval dễ đến mức baseline tụt từ 0,93 xuống 0,27 khi làm khó"
tension: tuong_ma_hoa_ra
sides: ["Baseline upstream đạt 0,93 trên bộ eval cũ", "Câu tìm trùng tiêu đề nên đạt điểm dù không bỏ dấu được, bộ khó chỉ còn 0,27"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Bộ eval sinh ra quá dễ: baseline upstream tụt từ 0,93 xuống 0,27

**Bối cảnh:** Corpus eval tiếng Việt sinh tự động, và baseline upstream đã đạt 0,93 trên hạng mục không dấu, nên điều kiện cải thiện gấp đôi không thể đạt.
**Chuyện gì xảy ra:** Điều tra cho thấy mỗi câu tìm trùng với tiêu đề note nên nhánh tiêu đề và nhánh vector tìm thấy dù FTS5 không bỏ dấu được. Làm lại corpus, mỗi cụm 25 note có cùng nội dung và khác một từ khoá, baseline hạng mục không dấu tụt từ 0,93 xuống 0,27 và hạng mục dd từ 0,87 xuống 0,40. Với corpus khó hơn điều kiện mới đạt được mà không hạ ngưỡng.
**Bài học:** Trước khi tin một bộ eval sinh ra, kiểm xem đáp án có lộ qua tiêu đề hoặc đường dẫn không; đo baseline trước là cách nhanh nhất để phát hiện.
**Artefact:** Bảng baseline trước và sau khi làm khó corpus, theo từng hạng mục. Không cần che.
**Góc người ngoài:** cách làm phổ biến là Thường chỉ đo bằng vài câu tự nghĩ, hoặc đưa dữ liệu thật lên CI để tiện; ở đây khác ở Phiên này phát hiện bộ đo tự sinh quá dễ (baseline tụt từ 0,93 xuống 0,27), và ghi kết quả chi tiết ra file ngoài repo kèm kiểm tra đường dẫn. Người đọc sẽ muốn biết làm sao vừa đo được vừa giữ riêng tư.
