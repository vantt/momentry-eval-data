---
id: 2026-11-02-corpus-tong-hop-qua-de-khien
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L315", "claude:c4caee3c#L1034", "claude:c4caee3c#L1044"]
hook: "Corpus dễ đến mức baseline đã đạt 0,93, cổng 'gấp đôi' không thể qua"
tension: tuong_ma_hoa_ra
sides: ["Tưởng FTS5 không bỏ dấu nên bài test khó", "Tiêu đề note trùng cụm tìm nên vẫn tìm ra; làm khó lại baseline còn 0,27"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Corpus tổng hợp quá dễ khiến cổng đo không bao giờ đạt được

**Bối cảnh:** Bộ eval tiếng Việt sinh tự động dùng để kiểm gói tiếng Việt. Mục tiêu G3 yêu cầu Hit@5 từ 0,85 trở lên và gấp đôi baseline upstream.
**Chuyện gì xảy ra:** Baseline upstream chưa có gói đã đạt Hit@5 0,93 ở vi-unaccented và 0,87 ở vi-dd, nên điều kiện gấp đôi không thể đạt. Nguyên nhân là mỗi cụm từ cần tìm cũng là tiêu đề note, nên nhánh vector và khớp tiêu đề tìm được note dù FTS5 không bỏ dấu. Agent đo trực tiếp unicode61 và thấy nó chỉ bỏ dấu khi syllable có một dấu, còn syllable hai dấu như ế, ữ, ợ, ặ và chữ đ thì không. Sau khi làm corpus khó hơn, baseline giảm còn 0,27 và 0,40.
**Bài học:** Trước khi đặt ngưỡng cải thiện, kiểm xem baseline có đã đạt không; nếu đã đạt thì bộ đo đang quá dễ, không phải phần mềm đã tốt.
**Artefact:** Bảng Hit@5 theo hạng mục trước và sau khi làm corpus khó hơn. Không chụp nội dung note hay câu hỏi.
