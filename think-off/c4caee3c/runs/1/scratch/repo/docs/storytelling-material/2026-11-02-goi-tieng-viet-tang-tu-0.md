---
id: 2026-11-02-goi-tieng-viet-tang-tu-0
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L1138", "claude:c4caee3c#L1150", "claude:c4caee3c#L1283", "claude:c4caee3c#L1952", "claude:c4caee3c#L2187"]
hook: "Câu tiếng Việt không dấu: nDCG@5 từ 0,133 lên 0,951"
tension: it_ma_nhieu
sides: ["Câu gõ không dấu gần như không tìm ra gì", "Sau các lớp bổ sung điểm vọt lên 0,951, Hit@5 đạt 1,00"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Gói tiếng Việt tăng từ 0,666 lên 0,932 qua các lần đo, đặc biệt câu không dấu

**Bối cảnh:** Gói tiếng Việt gồm chuẩn hoá, bỏ dấu, phục hồi dấu, Telex, sửa lỗi gõ và đồng nghĩa, chạy qua điểm cắm ngôn ngữ của fork.
**Chuyện gì xảy ra:** Số đo qua các giai đoạn: nDCG@5 tổng 0,666 của upstream lên 0,813 khi có V13, rồi 0,932 khi đủ các thành phần. vi-unaccented từ 0,133 lên 0,951 và Hit@5 từ 0,27 lên 1,00; vi-dd từ 0,263 lên 0,888. Với vi-alias, Hit@1 từ 0,60 lên 0,93 sau khi thêm view fold.
**Bài học:** Đo sau mỗi thành phần, không chỉ đo cuối cùng, để biết thành phần nào thật sự đóng góp.
**Artefact:** Bảng nDCG@5 và Hit@5 theo hạng mục, từ 0,666 đến 0,932.
