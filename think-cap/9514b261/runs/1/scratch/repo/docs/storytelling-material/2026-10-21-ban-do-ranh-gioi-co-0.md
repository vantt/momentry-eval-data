---
id: 2026-10-21-ban-do-ranh-gioi-co-0
date: 2026-10-21
repo: repo
status: raw
signals: [artefact, số trước/sau]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L970", "claude:9514b261#L971", "claude:9514b261#L986", "claude:9514b261#L997"]
hook: "Bản đồ ranh giới 686 dòng không có tên nào của năm component"
tension: tuong_ma_hoa_ra
sides: ["Tưởng bản đồ ranh giới đã bao phủ các component chính", "Năm tên đều 0 kết quả trong 686 dòng"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Bản đồ ranh giới có 0 dòng cho năm tên component đã nói đến

**Bối cảnh:** Người dùng hỏi các component trong kế hoạch có nằm trong bản đồ ranh giới của repo không. Agent đếm tên trong ba file bản đồ.
**Chuyện gì xảy ra:** Năm tên (Knowledge and Documentation Engine, Agent Context Engine, Effective Decision Reducer, Claim registry, và các tên decision projection) đều cho 0 kết quả ở ba file. Bản nháp bản đồ có 686 dòng nhưng cũng không có tên nào. Chỉ có một hàng gần nghĩa về registry tài liệu và không nhắc quyết định.
**Bài học:** Bản đồ ranh giới không tự cập nhật theo code; mỗi component mới cần một bước đăng ký hoặc ghi rõ không thay đổi bản đồ.
**Artefact:** Bảng 5 tên × 3 file bản đồ với toàn số 0, kèm ghi chú số dòng của bản nháp.
