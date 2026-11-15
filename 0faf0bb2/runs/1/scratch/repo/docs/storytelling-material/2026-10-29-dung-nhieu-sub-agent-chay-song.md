---
id: 2026-10-29-dung-nhieu-sub-agent-chay-song
date: 2026-10-29
repo: repo
status: raw
signals: []
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:0faf0bb2#L519", "claude:0faf0bb2#L520", "claude:0faf0bb2#L521", "claude:0faf0bb2#L577", "claude:0faf0bb2#L578", "claude:0faf0bb2#L1773", "claude:0faf0bb2#L1774", "claude:0faf0bb2#L1885", "claude:0faf0bb2#L1886"]
hook: "Nhiều agent đọc song song, nhưng mình vẫn tự grep lại từng trích dẫn"
tension: none
sides: []
strength: 1
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Dùng nhiều sub-agent chạy song song để đọc một codebase lạ theo các mảng (schema, runtime, UI, lịch sử), rồi tự kiểm lại các trích dẫn chính bằng sed/grep trước khi ghi kết luận

**Chuyện gì xảy ra:** Dùng nhiều sub-agent chạy song song để đọc một codebase lạ theo các mảng (schema, runtime, UI, lịch sử), rồi tự kiểm lại các trích dẫn chính bằng sed/grep trước khi ghi kết luận
**Góc người ngoài:** cách làm phổ biến là Dev đọc README, lướt vài file, hỏi AI tóm tắt cả repo trong một lượt rồi tin kết quả. Hiếm ai tách việc đọc theo chiều và đối chiếu số dòng; ở đây khác ở Mỗi mảng có agent riêng với câu hỏi cụ thể, kết quả có đường dẫn và số dòng, và bước xác minh lại trích dẫn giúp bắt lỗi bịa. Người đọc muốn có quy trình 'đọc repo nhanh mà đáng tin'.
