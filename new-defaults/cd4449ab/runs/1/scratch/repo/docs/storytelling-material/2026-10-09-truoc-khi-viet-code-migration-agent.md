---
id: 2026-10-09-truoc-khi-viet-code-migration-agent
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [outsider]
lines: ["omp:cd4449ab#L39", "omp:cd4449ab#L1377", "omp:cd4449ab#L1411", "omp:cd4449ab#L1462"]
hook: "Lập bảng ánh xạ từng trường trước khi viết dòng code migration nào"
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

# Trước khi viết code migration, agent lập bảng đối chiếu từng trường một: trường nào ở file v1 đi đâu ở file v3, được giữ, suy ra, hay bỏ, dựa trên struct Go và JSON schema.

**Chuyện gì xảy ra:** Trước khi viết code migration, agent lập bảng đối chiếu từng trường một: trường nào ở file v1 đi đâu ở file v3, được giữ, suy ra, hay bỏ, dựa trên struct Go và JSON schema.
**Góc người ngoài:** cách làm phổ biến là Hầu hết người dùng AI nhảy thẳng vào code rồi sửa theo lỗi gặp phải, ít khi lập bảng ánh xạ đầy đủ trước; ở đây khác ở Bảng này là tài liệu hợp đồng được commit cùng code. Người đọc sẽ hỏi cách tạo nó và tại sao nó đáng giá hơn việc chỉ viết test.
