---
id: 2026-11-03-reviewer-doc-lap-tim-16-loi
date: 2026-11-03
repo: repo
status: raw
signals: ["2", "4"]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2026", "claude:ab9a1dd8#L2039", "claude:ab9a1dd8#L2062", "claude:ab9a1dd8#L2079"]
hook: "Test xanh hết, reviewer vẫn tìm ra 16 lỗi"
tension: tuong_ma_hoa_ra
sides: ["bộ test đã xanh toàn bộ", "reviewer độc lập vẫn tìm ra 16 lỗi, 4 lỗi nặng"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Reviewer độc lập tìm 16 lỗi sau khi bộ test đã xanh

**Bối cảnh:** Test Linux qua 230 trên 230 và lifecycle installer qua. Agent gọi một subagent review độc lập đọc code.
**Chuyện gì xảy ra:** Reviewer báo 4 lỗi nặng, 5 trung bình, 7 nhẹ. Phần lớn nằm ở nhánh Windows và ở đường dẫn tuỳ chỉnh, những chỗ test Linux không chạy tới. Agent sửa hết trong phạm vi và thêm test cho từng lỗi.
**Bài học:** Test xanh trên một hệ điều hành không chứng minh được nhánh của hệ khác. Reviewer đọc theo hành vi của PowerShell và cmd tìm được lỗi mà test không thấy.
**Artefact:** Bảng 16 phát hiện với cột mức độ và tệp liên quan.
