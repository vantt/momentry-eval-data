---
id: 2026-11-06-de-tinh-anh-huong-cua-tung-f922
code: M-BR0S
aliases: [M-BR0S]
date: 2026-11-06
repo: repo
status: raw
signals: []
source: "chat Claude, claude:5a1e7c06"
sessions: ["claude:5a1e7c06"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:5a1e7c06#L33", "claude:5a1e7c06#L34", "claude:5a1e7c06#L35"]
hook: "Muốn biết mỗi thay đổi tốn bao nhiêu, đừng sửa bảng tính"
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

# Để tính ảnh hưởng của từng thay đổi (thêm dàn, mất cọc, hoàn vé), agent chạy script ngân sách với các tham số --them cộng dồn, thay vì sửa trực tiếp bảng tính.

**Chuyện gì xảy ra:** Để tính ảnh hưởng của từng thay đổi (thêm dàn, mất cọc, hoàn vé), agent chạy script ngân sách với các tham số --them cộng dồn, thay vì sửa trực tiếp bảng tính.
**Góc người ngoài:** cách làm phổ biến là Sửa trực tiếp file ngân sách hoặc tính nhẩm từng khoản rồi cộng lại; ở đây khác ở Mỗi giả định là một dòng lệnh có thể chạy lại, và file gốc không bị đụng tới. Khi user đổi ý, chỉ cần thêm hoặc bớt một tham số là tính lại được ngay.
