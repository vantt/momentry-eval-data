---
id: 2026-10-21-phase-ghi-completed-nhung-khong-co
date: 2026-10-21
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L1417", "claude:9514b261#L1523"]
hook: "Phase ghi 'completed' nhưng file hứa làm không hề tồn tại"
tension: cam_ma_van_lot
sides: ["Phase 12 đánh dấu đã xong, cảnh báo đã có", "Không có file, và 332 doc quá hạn không ai nhắc"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Phase ghi completed nhưng không có file bằng chứng

**Bối cảnh:** Một kế hoạch cũ đã lưu trữ, nhưng vẫn được đánh dấu hoàn thành.
**Chuyện gì xảy ra:** Phase 12 ghi completed, nhưng file spec mà nó hứa không tồn tại, và tài liệu vẫn giữ quy tắc cũ. Ở registry, check doc-provisional-aged không bao giờ bắn, vì so sánh chuỗi ISO với số làm ra NaN. Kết quả: 332 doc đã quá 47 đến 55 ngày vẫn không được ai nhắc.
**Bài học:** Đánh dấu hoàn thành phải kèm đường dẫn file. Check dựa trên tuổi cần so sánh đúng kiểu dữ liệu.
**Artefact:** Bảng: phase | trạng thái ghi | file có tồn tại không.
