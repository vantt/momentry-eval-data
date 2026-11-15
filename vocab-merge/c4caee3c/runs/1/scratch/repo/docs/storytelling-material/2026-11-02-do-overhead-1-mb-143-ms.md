---
id: 2026-11-02-do-overhead-1-mb-143-ms
date: 2026-11-02
repo: repo
status: raw
signals: [số trước sau, ràng buộc định hình thiết kế]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L1801", "claude:c4caee3c#L1820", "claude:c4caee3c#L1833"]
hook: "Cùng một bài test: 143 ms trên máy, 318 ms trên CI"
tension: tuong_ma_hoa_ra
sides: ["Ngưỡng 200 ms tưởng là cố định", "Runner chậm gấp đôi nên đỏ, phải nhân ngưỡng x3 trong CI"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đo overhead 1 MB: 143 ms trên máy, 318 ms trên runner, nhân ngưỡng x3 thay vì nới gốc

**Bối cảnh:** PRD đặt ngưỡng 200 ms cho project trên 1 MB.
**Chuyện gì xảy ra:** Trên runner GitHub đo được 318 ms, vượt 200 ms. Thêm biến OHS_PERF_FACTOR đặt bằng 3 trong CI, mặc định bằng 1 trên máy thật nên vẫn kiểm đúng ngưỡng PRD. Test lấy lần nhanh nhất trong ba lần chạy.
**Bài học:** Ngưỡng hiệu năng nên có hệ số cho CI nhưng giữ giá trị gốc trên máy người dùng; đừng hạ ngưỡng.
