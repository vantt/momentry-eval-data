---
id: 2026-10-09-agent-doc-schema-va-go-struct
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, outsider]
lines: ["omp:cd4449ab#L1", "omp:cd4449ab#L1364", "omp:cd4449ab#L1712", "omp:cd4449ab#L2024"]
hook: "Trước khi code, agent lập bảng ánh xạ từng trường làm bằng chứng"
tension: none
sides: []
strength: 0
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent đọc schema và Go struct để lập bảng ánh xạ từng trường v1 sang v3 trước khi viết code, và bảng này được lead chấp nhận như bằng chứng

**Chuyện gì xảy ra:** Agent đọc schema và Go struct để lập bảng ánh xạ từng trường v1 sang v3 trước khi viết code, và bảng này được lead chấp nhận như bằng chứng
**Góc người ngoài:** cách làm phổ biến là Đọc tài liệu rồi code thẳng, ánh xạ trường ngầm trong đầu; ở đây khác ở Bảng ánh xạ 19 trường có cột bằng chứng là file:dòng và trạng thái (kept/derived/dropped). Người đọc sẽ hỏi cách làm bảng đối chiếu như vậy để review thay đổi định dạng dữ liệu.
