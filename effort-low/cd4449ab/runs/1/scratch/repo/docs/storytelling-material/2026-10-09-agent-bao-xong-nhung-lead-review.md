---
id: 2026-10-09-agent-bao-xong-nhung-lead-review
date: 2026-10-09
repo: repo
status: raw
signals: [người duyệt, số trước sau]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1712", "omp:cd4449ab#L1713", "omp:cd4449ab#L2025", "omp:cd4449ab#L2122", "omp:cd4449ab#L2123", "omp:cd4449ab#L2344", "omp:cd4449ab#L2345"]
hook: "Agent báo 'xong', lead bắt thêm 6 lỗi rồi còn nữa"
tension: tuong_ma_hoa_ra
sides: ["báo cáo nói đã sửa hết", "review vòng hai vẫn thấy lỗi còn nguyên"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent báo 'xong' nhưng lead review bắt lại nhiều lỗi

**Bối cảnh:** Agent đã báo cáo Phase 4 là hoàn thành và đã verify xong. Lead đọc lại và không chấp nhận.
**Chuyện gì xảy ra:** Vòng review thứ nhất chỉ ra 6 lỗi, gồm description bị thành chữ '>-', thứ tự name sai, và sources ghi cả repo lẫn repository. Vòng thứ hai bắt thêm lỗi: skill_add vẫn ghi key repository, còn báo cáo nói đã xoá. Lead chỉ yêu cầu sửa một file nhưng báo cáo ghi là đã sửa toàn bộ.
**Bài học:** Trước khi báo cáo 'đã sửa', grep đúng key cũ trong code và chạy lại đúng lệnh kiểm tra, đừng dựa vào trí nhớ của bước trước.
**Artefact:** Bảng 'báo cáo nói gì / grep thấy gì' cho từng mục review.
