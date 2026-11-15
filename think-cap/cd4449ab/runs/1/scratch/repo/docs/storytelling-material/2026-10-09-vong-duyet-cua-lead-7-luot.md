---
id: 2026-10-09-vong-duyet-cua-lead-7-luot
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest]
lines: ["omp:cd4449ab#L1462", "omp:cd4449ab#L1713", "omp:cd4449ab#L2025", "omp:cd4449ab#L2123", "omp:cd4449ab#L2345", "omp:cd4449ab#L2374", "omp:cd4449ab#L3656"]
hook: "Lead duyệt 7 lượt, lượt nào cũng bắt đúng thứ máy tin"
tension: tuong_ma_hoa_ra
sides: ["Máy báo xong, make check xanh", "Người duyệt bắt thêm lỗi ở cả 7 lượt"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Vòng duyệt của lead: 7 lượt, mỗi lượt bắt thứ máy tin

**Bối cảnh:** Phase 4 và phần đầu Phase 3 của worktree C đi qua vòng duyệt của lead, mỗi lượt có danh sách sửa cụ thể.
**Chuyện gì xảy ra:** Lead gửi ít nhất 7 lượt phản hồi. Lượt đầu nói NOT mergeable vì migration thật lỗi ở v1→v2. Các lượt sau bắt mô tả thành '>-', tên sai thứ tự, ghi cả repo lẫn repository, một writer còn layout cũ, và lỗi WalkDir bị nuốt. Mỗi lượt đều yêu cầu test-first và make check xanh trước commit.
**Bài học:** Người đọc diff thật và chạy trên bản sao dữ liệu thật tìm được lỗi mà self-review của agent bỏ qua.
**Artefact:** Bảng 7 lượt phản hồi: lỗi bắt được và commit sửa, che tên người.
