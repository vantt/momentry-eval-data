---
id: 2026-10-21-giao-nghien-cuu-cho-ba-agent
date: 2026-10-21
repo: repo
status: raw
signals: []
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:9514b261#L1347", "claude:9514b261#L1384", "claude:9514b261#L1529", "claude:9514b261#L1536"]
hook: "Ba AI quét ba mảng, và báo cả chỗ số liệu lệch nhau"
tension: hop_ma_tan
sides: ["Ba agent chạy song song, mỗi người một mảng", "Bản tổng hợp lộ ra số liệu lệch giữa họ"]
strength: 1
stakes: 2
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Giao nghiên cứu cho ba agent chạy song song, mỗi agent quét một mảng (plans/reports, history/journals, work items/code/specs) và ghi báo cáo riêng. Sau đó một bản tổng hợp gộp lại và ghi rõ chỗ số liệu lệch giữa các agent.

**Chuyện gì xảy ra:** Giao nghiên cứu cho ba agent chạy song song, mỗi agent quét một mảng (plans/reports, history/journals, work items/code/specs) và ghi báo cáo riêng. Sau đó một bản tổng hợp gộp lại và ghi rõ chỗ số liệu lệch giữa các agent.
**Góc người ngoài:** cách làm phổ biến là Hỏi một AI duy nhất trong một cuộc chat dài, hoặc tự đọc tài liệu rồi tóm tắt theo trí nhớ; ở đây khác ở Kết quả được chia theo nguồn để kiểm tra được, và các mâu thuẫn giữa agent được nêu ra thay vì bị gộp mất. Người đọc muốn biết cách phân mảng việc và chống trùng lặp khi nhiều agent cùng đọc một kho.
