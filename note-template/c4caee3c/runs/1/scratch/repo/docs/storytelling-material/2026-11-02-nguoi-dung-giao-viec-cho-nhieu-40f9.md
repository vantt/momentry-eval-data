---
id: 2026-11-02-nguoi-dung-giao-viec-cho-nhieu-40f9
code: M-C5VQ
aliases: [M-C5VQ]
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:c4caee3c#L153", "claude:c4caee3c#L412", "claude:c4caee3c#L757", "claude:c4caee3c#L956", "claude:c4caee3c#L1075", "claude:c4caee3c#L1094"]
hook: "Nhiều agent chạy song song trên một repo, lead ghép lại từng bước"
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

# Người dùng giao việc cho nhiều agent chạy song song trên cùng một repo, mỗi agent có worktree riêng, rồi lead ghép các nhánh về chuỗi bản vá theo thứ tự phụ thuộc và kiểm lại toàn chuỗi sau mỗi lần ghép.

**Chuyện gì xảy ra:** Người dùng giao việc cho nhiều agent chạy song song trên cùng một repo, mỗi agent có worktree riêng, rồi lead ghép các nhánh về chuỗi bản vá theo thứ tự phụ thuộc và kiểm lại toàn chuỗi sau mỗi lần ghép.
**Góc người ngoài:** cách làm phổ biến là Đa số người dùng một mình chạy một AI tại một thời điểm, sửa trực tiếp trên nhánh chính, không tách việc song song kiểu này; ở đây khác ở Phiên này có 11+ agent chạy đồng thời, đẩy kết quả qua bản vá, xuất lại chuỗi và kiểm từng bước. Người đọc sẽ muốn biết cách điều phối nhiều agent mà không đạp lên nhau.
