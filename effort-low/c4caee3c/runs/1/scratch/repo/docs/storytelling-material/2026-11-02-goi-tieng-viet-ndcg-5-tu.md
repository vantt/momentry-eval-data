---
id: 2026-11-02-goi-tieng-viet-ndcg-5-tu
date: 2026-11-02
repo: repo
status: raw
signals: [số trước sau]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L1138", "claude:c4caee3c#L1952", "claude:c4caee3c#L2187"]
hook: "Tiếng Việt từ 0,666 lên 0,954 nhờ xếp nhiều lớp nhỏ, tiếng Anh vẫn 0,735"
tension: hop_ma_tan
sides: ["Nhiều lớp xử lý chồng lên nhau, điểm tiếng Việt tăng", "Tiếng Anh giữ nguyên 0,735 qua mọi bước"]
strength: 1
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Gói tiếng Việt: nDCG@5 từ 0,666 lên 0,932 qua nhiều lớp

**Bối cảnh:** Gói ngôn ngữ tiếng Việt được xây dựng từng bước trên điểm cắm chung của lõi.
**Chuyện gì xảy ra:** Lớp chuẩn hoá và fold đưa tổng nDCG@5 từ 0,666 lên 0,813. Hạng mục không dấu tăng từ 0,133 lên 0,951. Sau khi thêm tách từ, lexicon và alias tổng đạt 0,932, và đến bước cuối đạt 0,954 khi bật khôi phục dấu cho embedding. Hạng mục tiếng Anh giữ nguyên 0,735 qua mọi bước.
**Bài học:** Đo tổng và từng hạng mục sau mỗi lớp; chỉ tổng thì không lộ được hạng mục nào tụt.
**Artefact:** Biểu đồ nDCG@5 theo từng lớp của gói, tách hạng mục. Không cần che.
