---
id: 2026-10-09-pipeline-sua-theo-duoi-day-lead
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [outsider]
lines: ["omp:cd4449ab#L235", "omp:cd4449ab#L1363", "omp:cd4449ab#L1462", "omp:cd4449ab#L2025", "omp:cd4449ab#L2123", "omp:cd4449ab#L2124"]
hook: "Mỗi trường cũ ghi rõ Kept, Derived hay bỏ, kèm bằng chứng"
tension: none
sides: []
strength: 0
stakes: 2
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Pipeline sửa theo 'Dưới đây lead xem lại, agent sửa test-first' với bản đồ đích cho từng trường (field destination table) ghi vào plan: mỗi trường cũ được Kept, Derived hay bị bỏ, kèm bằng chứng đã xác minh trong code

**Chuyện gì xảy ra:** Pipeline sửa theo 'Dưới đây lead xem lại, agent sửa test-first' với bản đồ đích cho từng trường (field destination table) ghi vào plan: mỗi trường cũ được Kept, Derived hay bị bỏ, kèm bằng chứng đã xác minh trong code
**Góc người ngoài:** cách làm phổ biến là Đổi schema rồi cập nhật code, ghi chú migration nếu nhớ; ở đây khác ở Bảng này buộc kiểm kê từng trường trước khi đổi, bắt được trường bị bỏ sót như content_digest. Lead còn dùng nó để tìm bất nhất giữa các writer (skill_add, source_import, backfill), mà người đọc dễ gặp khi đổi định dạng lưu trữ.
