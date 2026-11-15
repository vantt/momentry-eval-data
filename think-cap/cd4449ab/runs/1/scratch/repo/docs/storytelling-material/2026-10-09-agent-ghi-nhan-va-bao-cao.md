---
id: 2026-10-09-agent-ghi-nhan-va-bao-cao
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [outsider]
lines: ["omp:cd4449ab#L1462", "omp:cd4449ab#L2122"]
hook: "Bảng mapping viết từ trí nhớ, chưa ai đối chiếu với code"
tension: tuong_ma_hoa_ra
sides: ["Bảng trông đúng vì viết từ tài liệu", "Chỉ đối chiếu từng field với code mới biết đúng"]
strength: 1
stakes: 0
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent ghi nhận và báo cáo rằng việc đối chiếu trường từng field với struct Go và JSON schema là bước xác minh bắt buộc trước khi kết luận một bảng mapping đã đúng.

**Chuyện gì xảy ra:** Agent ghi nhận và báo cáo rằng việc đối chiếu trường từng field với struct Go và JSON schema là bước xác minh bắt buộc trước khi kết luận một bảng mapping đã đúng.
**Góc người ngoài:** cách làm phổ biến là Dev thường viết bảng mapping từ trí nhớ hoặc từ tài liệu, ít khi đối chiếu từng dòng với code thật; ở đây khác ở Đối chiếu từng hàng với nguồn sự thật (code và schema) làm bảng có bằng chứng. Người đọc muốn biết cách làm này có thể áp dụng cho tài liệu thiết kế khác.
