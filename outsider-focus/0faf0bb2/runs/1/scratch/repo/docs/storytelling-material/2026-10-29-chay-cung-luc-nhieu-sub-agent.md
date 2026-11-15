---
id: 2026-10-29-chay-cung-luc-nhieu-sub-agent
date: 2026-10-29
repo: repo
status: raw
signals: []
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:0faf0bb2#L564", "claude:0faf0bb2#L577", "claude:0faf0bb2#L1584", "claude:0faf0bb2#L1773", "claude:0faf0bb2#L1837", "claude:0faf0bb2#L1885", "claude:0faf0bb2#L3814", "claude:0faf0bb2#L3883"]
hook: "Bốn codebase, một bộ câu hỏi, mỗi agent tự mở lại trích dẫn"
tension: none
sides: []
strength: 0
stakes: 0
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chạy cùng lúc nhiều sub-agent, mỗi agent đọc một codebase theo cùng bộ câu hỏi, rồi tự mở lại các trích dẫn chính trước khi ghi kết luận. Dùng cho việc so sánh Paperclip, AICoworker, Multica và Kaneo theo tiêu chí giống nhau.

**Chuyện gì xảy ra:** Chạy cùng lúc nhiều sub-agent, mỗi agent đọc một codebase theo cùng bộ câu hỏi, rồi tự mở lại các trích dẫn chính trước khi ghi kết luận. Dùng cho việc so sánh Paperclip, AICoworker, Multica và Kaneo theo tiêu chí giống nhau.
**Góc người ngoài:** cách làm phổ biến là Dev đọc từng repo một, hoặc hỏi AI một câu tổng quát rồi tin câu trả lời. Ít khi chia việc song song theo từng hệ thống với cùng một khung câu hỏi; ở đây khác ở Đánh giá 4 repo lớn (nhiều nghìn commit) trong vài chục phút mà vẫn có bằng chứng kiểm chứng được. Người đọc có thể áp dụng khi chọn thư viện hay framework, và bước tự kiểm lại trích dẫn chặn được việc sub-agent bịa số dòng.
