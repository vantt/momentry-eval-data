---
id: 2026-11-02-stop-hook-giu-agent-khong-dung-3c6e
code: M-Q98D
aliases: [M-Q98D]
date: 2026-11-02
repo: repo
status: raw
signals: [rang_buoc_thiet_ke, khac]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:2dfb5915#L477", "claude:2dfb5915#L2147", "claude:2dfb5915#L2590", "claude:2dfb5915#L2872"]
hook: "Hook giữ agent lại gần 30 lần để đòi việc chỉ người mới làm được"
tension: gap_ma_phai_chon
sides: ["Hook đòi xong toàn bộ plan", "Còn cổng của người, agent không thể làm gì thêm"]
strength: 3
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Stop hook giữ agent không dừng suốt nhiều vòng: điều kiện 'xong toàn bộ plan' không thể đạt khi còn cổng của người

**Bối cảnh:** Mục tiêu được đặt thành xong toàn bộ plan kèm yêu cầu cập nhật, commit và push sau mỗi mục. Plan có các cổng chờ người và chờ máy Windows.
**Chuyện gì xảy ra:** Hook chặn dừng gần 30 lần, mỗi lần agent trả lời là chưa thể làm gì thêm và đang chờ. Người dùng thu hẹp phạm vi xuống 'tới khi cài được', nhưng hook vẫn đòi toàn bộ plan. Agent có soạn một báo cáo lỗi cho hook nhưng không gửi. Lối thoát duy nhất là người dùng xoá goal.
**Bài học:** Đặt điều kiện dừng phải khớp phạm vi thật của công việc; nếu phần còn lại phụ thuộc người khác, hãy ghi rõ điều kiện đó ngay từ đầu.
**Artefact:** Chuỗi thông báo hook lặp lại (có thể dán một đoạn ngắn). Không đưa nội dung plan.
