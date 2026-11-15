---
id: 2026-10-21-chay-3-agent-nghien-cuu-song
date: 2026-10-21
repo: repo
status: raw
signals: []
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:9514b261#L1329", "claude:9514b261#L1347", "claude:9514b261#L1384", "claude:9514b261#L1399", "claude:9514b261#L1432", "claude:9514b261#L1477", "claude:9514b261#L1523"]
hook: "Ba agent chạy song song, nhưng số liệu then chốt vẫn do em tự grep lại"
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

# Chạy 3 agent nghiên cứu song song, mỗi agent quét một mảng và ghi báo cáo riêng. Trước khi giao, chạy một lệnh kiểm để chọn cách chạy. Khi cả ba xong, agent chính tự kiểm lại các con số then chốt bằng grep hoặc đọc file gốc, rồi mới gộp thành một bản tổng hợp và nêu rõ phần nào đã kiểm, phần nào chỉ là suy luận.

**Chuyện gì xảy ra:** Chạy 3 agent nghiên cứu song song, mỗi agent quét một mảng và ghi báo cáo riêng. Trước khi giao, chạy một lệnh kiểm để chọn cách chạy. Khi cả ba xong, agent chính tự kiểm lại các con số then chốt bằng grep hoặc đọc file gốc, rồi mới gộp thành một bản tổng hợp và nêu rõ phần nào đã kiểm, phần nào chỉ là suy luận.
**Góc người ngoài:** cách làm phổ biến là Giao một câu hỏi cho một AI, đọc câu trả lời và tin luôn. Nếu có nhiều agent thì chúng thường ghi chung một chỗ, và không ai kiểm lại số liệu trước khi chuyển tiếp; ở đây khác ở Người đọc sẽ hỏi làm sao để nhiều agent không ghi đè lên nhau và làm sao biết báo cáo có đúng. Điểm khác là mỗi agent có một file riêng, chỉ được đọc và chỉ ghi một file, còn người điều phối kiểm lại từng con số trước khi báo lại.
