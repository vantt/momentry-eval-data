---
id: 2026-11-02-goi-tieng-viet-ndcg-5-tong
date: 2026-11-02
repo: repo
status: raw
signals: ["Số trước, số sau"]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L1138", "claude:c4caee3c#L1150", "claude:c4caee3c#L1672", "claude:c4caee3c#L1952", "claude:c4caee3c#L2187"]
hook: "Thêm từng lớp xử lý tiếng Việt, nDCG@5 từ 0,666 lên 0,932"
tension: hop_ma_tan
sides: ["gộp từng lớp xử lý vào gói", "điểm tăng liên tục, không hạng mục nào tụt"]
strength: 1
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Gói tiếng Việt: nDCG@5 tổng từ 0,666 lên 0,932 qua từng lớp

**Bối cảnh:** Gói tiếng Việt chạy trên điểm cắm P01 và được cộng dần từng lớp: dấu, Telex, gõ sai, đồng nghĩa, viết tắt, alias, tách từ.
**Chuyện gì xảy ra:** Lần đo đầu với gói đủ M2 và M3: nDCG@5 tổng từ 0,666 lên 0,813, vi-unaccented Hit@5 từ 0,27 lên 1,00, vi-dd từ 0,40 lên 1,00. Các lớp sau đưa tổng lên 0,932. Không hạng mục nào tụt, eval tiếng Anh giữ 0,735.
**Bài học:** Đo sau từng lớp và ghi bảng trước và sau mới biết lớp nào thật sự đáng giá.
**Artefact:** Bảng so baseline với gói ở từng bước theo hạng mục. Không có nội dung note.
