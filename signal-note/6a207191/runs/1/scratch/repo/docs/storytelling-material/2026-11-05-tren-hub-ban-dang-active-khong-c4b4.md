---
id: 2026-11-05-tren-hub-ban-dang-active-khong-c4b4
code: M-TYTV
aliases: [M-TYTV]
date: 2026-11-05
repo: repo
status: raw
signals: []
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:6a207191#L1500", "claude:6a207191#L1503", "claude:6a207191#L1515"]
hook: "Hub đang chạy bản cũ, bản vừa sửa chưa ai duyệt"
tension: tuong_ma_hoa_ra
sides: ["Ai cũng tin máy chủ chạy bản vừa sửa", "Diff từng file cho thấy đang chạy bản duyệt cũ"]
strength: 3
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Trên hub, bản đang active không khớp với thư mục skill trên máy này. Agent tải bản hub về, diff từng file, rồi báo rằng bản duyệt cũ đã được áp dụng mà không ai bấm duyệt bản mới.

**Chuyện gì xảy ra:** Trên hub, bản đang active không khớp với thư mục skill trên máy này. Agent tải bản hub về, diff từng file, rồi báo rằng bản duyệt cũ đã được áp dụng mà không ai bấm duyệt bản mới.
**Góc người ngoài:** cách làm phổ biến là Người dùng thường tin rằng máy chủ đang chạy đúng bản họ vừa sửa, và chỉ phát hiện khi có chuyện hỏng; ở đây khác ở Agent không đoán mà đối chiếu nguồn thật (bản đang phục vụ) với bản cục bộ, rồi tách rõ hai thứ là bản gửi chờ duyệt và bản đang chạy. Người đọc sẽ muốn biết cách biết chắc máy nào đang phục vụ gì.
