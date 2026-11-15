---
id: 2026-10-21-ba-agent-quet-song-song-knowledge-fd46
code: M-04ZP
aliases: [M-04ZP]
date: 2026-10-21
repo: repo
status: raw
signals: [khac, nguyen_nhan_bat_ngo, nguoi_duyet_may_soan]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:9514b261#L1325", "claude:9514b261#L1384", "claude:9514b261#L1398", "claude:9514b261#L1417", "claude:9514b261#L1457", "claude:9514b261#L1476", "claude:9514b261#L1572", "claude:9514b261#L1582"]
hook: "Đề xuất mới suýt trùng: registry đã chạy sẵn trên 479 tài liệu"
tension: tuong_ma_hoa_ra
sides: ["Tưởng cần đề xuất xây mới một registry", "Registry đã có 479 doc, lỗi gốc chỉ là so chuỗi ngày ra NaN"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Ba agent quét song song: Knowledge Registry đã chạy trên 479 tài liệu, đề xuất mới suýt trùng

**Bối cảnh:** Chủ nghi kho quản lý tài liệu trong đề xuất Knowledge and Documentation Engine đã có một hệ tương tự xây trước đó. Agent chạy ba researcher song song, mỗi người quét một mảng.
**Chuyện gì xảy ra:** Registry có 479 topic và 479 doc, chỉ phủ tài liệu end-user, khoảng 15% trong 3146 file .md. Có ba index song song với 492, 479 và 0 mục. Trong 479 doc có 332 provisional và 147 active, với 365 role khác nhau. Lỗi gốc nhỏ: check doc-provisional-aged không bao giờ bắn, vì so updatedAt là chuỗi ISO nên ra NaN. Agent kiểm lại từng con số trước khi gộp rồi ghi 25 dòng ghi chú vào proposal.
**Bài học:** Trước khi đề xuất component mới, hãy đếm xem thứ tương tự đã chạy chưa. Một check trả NaN im lặng còn nguy hiểm hơn việc không có check.
**Artefact:** Bản tổng hợp ba báo cáo và bảng số liệu các index. Không cần ảnh.
