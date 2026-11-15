---
id: 2026-10-09-77-commit-sha-ngan-trong-distill
date: 2026-10-09
repo: repo
status: raw
signals: [số trước sau, nguyên nhân bất ngờ]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest]
lines: ["omp:cd4449ab#L2414", "omp:cd4449ab#L2416", "omp:cd4449ab#L2440", "omp:cd4449ab#L2456", "omp:cd4449ab#L2458", "omp:cd4449ab#L2461", "omp:cd4449ab#L2491"]
hook: "77 mã commit bị cắt ngắn, và cả 77 đều tìm lại được"
tension: khac
sides: ["SHA rút gọn tưởng đã mất thông tin", "mirror khôi phục đủ 77/77 thành 40 ký tự"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# 77 commit SHA ngắn trong distill.yaml phải mở rộng qua git mirror

**Bối cảnh:** File distill giai đoạn 0 có 1184 dòng, 46161 byte, 42 lesson. Mỗi evidence ghi commit ở dạng SHA rút gọn.
**Chuyện gì xảy ra:** Đếm được 77 entry SHA rút gọn trong 2 repo. Dùng git rev-parse trên mirror để mở rộng, ví dụ một SHA 12 ký tự ra 40 ký tự. Mọi SHA đều resolve được trên mirror, nên migration có thể đổi thành tham chiếu đầy đủ mà không mất thông tin.
**Bài học:** SHA rút gọn trông như khoá nhưng thực ra mơ hồ; trước khi lưu, mở rộng nó về dạng đầy đủ bằng git.
**Artefact:** Bảng SHA rút gọn và SHA đầy đủ tương ứng (che tên repo).
