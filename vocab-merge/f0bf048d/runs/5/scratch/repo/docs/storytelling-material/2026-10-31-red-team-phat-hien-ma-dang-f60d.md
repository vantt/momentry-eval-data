---
id: 2026-10-31-red-team-phat-hien-ma-dang-f60d
code: M-YNN4
aliases: [M-YNN4]
date: 2026-10-31
repo: repo
status: raw
signals: [người duyệt máy, nguyên nhân gốc nhỏ]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:f0bf048d#L1855", "claude:f0bf048d#L1875", "claude:f0bf048d#L1878", "claude:f0bf048d#L1891", "claude:f0bf048d#L1975"]
hook: "Mã đăng nhập 6 ký tự nằm trong .env, ai biết email là thành chủ"
tension: nho_ma_to
sides: ["Một mã dev 6 ký tự trong cấu hình", "Có thể mở cửa đăng nhập thành chủ tài khoản"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Red-team phát hiện mã đăng nhập dev 6 ký tự còn trong .env, kéo theo ba lỗ khẩn

**Bối cảnh:** Đã viết tài liệu thiết kế quyền cho agent. Một agent độc lập, model khác, được giao phản biện ở chế độ chỉ đọc.
**Chuyện gì xảy ra:** Phản biện tìm ra mã đăng nhập dev 6 ký tự trong cấu hình backend. Nếu còn hiệu lực thì ai gọi được API và biết email chủ có thể đăng nhập thành chủ, hoặc dò tối đa 10 mũ 6 khả năng. Tôi kiểm lại bằng grep chỉ đọc độ dài, không in giá trị: mã đã trống trong container đang chạy. Harness còn gắn cờ kết quả phản biện là giống chỉ dẫn; xử lý nó như phát hiện để báo lại, không làm theo.
**Bài học:** Để một agent độc lập phản biện thiết kế quyền, và kiểm từng phát hiện bằng cách đọc cấu hình thật mà không in bí mật.
**Artefact:** Bảng xếp hạng lỗ hổng (che giá trị bí mật).
**Góc người ngoài:** cách làm phổ biến là Chạy agent dưới chính tài khoản của dev cho tiện, dùng chung token; ở đây khác ở Phiên này dùng red-team để tìm lỗ hổng trước khi làm. Người đọc muốn biết cách đặt câu hỏi "nếu agent bị điều khiển thì sao" và cách xử lý.
