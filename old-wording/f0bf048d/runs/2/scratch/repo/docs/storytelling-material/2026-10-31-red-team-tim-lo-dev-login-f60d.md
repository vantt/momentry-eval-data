---
id: 2026-10-31-red-team-tim-lo-dev-login-f60d
code: M-5ECK
aliases: [M-5ECK]
date: 2026-10-31
repo: repo
status: raw
signals: [nguoi_duyet_may_soan, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L1855", "claude:f0bf048d#L1874", "claude:f0bf048d#L1875", "claude:f0bf048d#L1878", "claude:f0bf048d#L1975"]
hook: "Mã đăng nhập dev 6 ký tự có thể biến người lạ thành chủ"
tension: nho_ma_to
sides: ["chỉ là một mã 6 ký tự trong file .env", "ai biết email chủ có thể đăng nhập thành chủ"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Red-team tìm lỗ dev login code: chủ bị giả mạo qua API

**Bối cảnh:** Bản thiết kế quyền cho agent được nhờ một agent độc lập phản biện. Agent này chạy trên model khác.
**Chuyện gì xảy ra:** Phản biện chỉ ra file .env của Multica có mã đăng nhập dev 6 ký tự. Nếu mã còn hiệu lực, ai gọi được API và biết email chủ có thể đăng nhập thành chủ. Agent tự kiểm lại: biến này còn trong .env nhưng trống trong container đang chạy. Phiên song song đã xoá mã đăng nhập cố định ở commit khác. Phần đăng nhập bằng email vẫn còn, giới hạn 5 lần thử mỗi mã và 1 mã mỗi phút. Harness cũng gắn cờ output của subagent có mẫu lệnh và trung hoà các thẻ điều khiển.
**Bài học:** Phản biện bằng agent khác có giá trị, nhưng mỗi phát hiện cần tự kiểm trên máy trước khi đưa vào tài liệu.
**Artefact:** Đoạn phản biện đã biên tập, bỏ mọi giá trị bí mật.
