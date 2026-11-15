---
id: 2026-11-02-ci-do-tren-ca-ba-os-3c6e
code: M-5Q91
aliases: [M-5Q91]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1264", "claude:2dfb5915#L1283", "claude:2dfb5915#L1364"]
hook: "CI đỏ ba hệ điều hành, máy local thì xanh"
tension: tuong_ma_hoa_ra
sides: ["Cache tăng tốc build, local chạy không lỗi", "Cache xoá file dump, CI thoát mã 2 trên cả ba OS"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án là công cụ dòng lệnh viết lại bằng Rust để hỏi Claude Desktop về graph vault Obsidian, và người làm đang cố hoàn tất bản port lõi. CI đỏ trên Linux và macOS khi bước so sánh thoát mã 2, còn máy cục bộ vẫn xanh. Nguyên nhân là cache CI không chỉ tăng tốc build: nó xoá file ngoài thư mục build, để lại thư mục dump rỗng khiến bước kiểm tra từ chối ghi. Ai dùng cache để chứa dữ liệu kiểm thử đều có thể gặp đúng lỗi này."
audience: dev dùng CI cache khi test công cụ dòng lệnh
spine_context: "Một công cụ dòng lệnh để hỏi Claude Desktop về graph vault Obsidian, đang được viết lại bằng Rust; người làm đang hoàn tất bản port lõi."
spine_context_lines: [profile]
spine_want: Muốn hoàn tất plan rust-core-port và giữ CI xanh trên main.
spine_want_lines: ["claude:2dfb5915#L11"]
spine_obstacle: "CI đỏ trên Linux và macOS ở bước so bản Rust với golden, thoát mã 2."
spine_obstacle_lines: ["claude:2dfb5915#L1265", "claude:2dfb5915#L1272"]
spine_turn: "Tưởng cache CI chỉ tăng tốc build; hoá ra rust-cache xoá mọi file ngoài thư mục build cargo, để lại thư mục dump rỗng, nên bước kiểm tra từ chối ghi và thoát mã 2."
spine_turn_lines: ["claude:2dfb5915#L1364"]
spine_action: Ghi dump ra thư mục tạm ngoài cache trong ci.yml; thêm --no-fail-fast cho bước test.
spine_action_lines: ["claude:2dfb5915#L1364", "claude:2dfb5915#L1372"]
spine_outcome: Ba lỗi đã sửa thành commit trên main nhưng chưa push; bản sửa cho Windows chưa chạy trên máy Windows.
spine_outcome_lines: ["claude:2dfb5915#L1364"]
spine_takeaway: Đừng dùng thư mục cache để chứa dữ liệu kiểm thử; cache có thể đổi nội dung theo cách không ngờ.
spine_takeaway_lines: ["claude:2dfb5915#L1364"]
completeness: 7
---

# CI đỏ trên cả ba OS vì cache xoá file dump, và tên vault trên Windows bị sai

**Góc kể:** Dự án là công cụ dòng lệnh viết lại bằng Rust để hỏi Claude Desktop về graph vault Obsidian, và người làm đang cố hoàn tất bản port lõi. CI đỏ trên Linux và macOS khi bước so sánh thoát mã 2, còn máy cục bộ vẫn xanh. Nguyên nhân là cache CI không chỉ tăng tốc build: nó xoá file ngoài thư mục build, để lại thư mục dump rỗng khiến bước kiểm tra từ chối ghi. Ai dùng cache để chứa dữ liệu kiểm thử đều có thể gặp đúng lỗi này.
**Bối cảnh:** Bước parity của CI dùng rust-cache để lưu thư mục target.
**Chuyện gì xảy ra:** Rust-cache lưu target nhưng xoá mọi file ngoài thư mục build của cargo, chỉ giữ lại các thư mục rỗng. Từ lần chạy sau, cache được khôi phục khớp chính xác nên bước check thấy thư mục dump không rỗng mà không có manifest, từ chối ghi đè và thoát mã 2 trên cả ba OS. Chạy cục bộ thì không lỗi vì không ai xoá target. Ở lỗi thứ hai, hàm basename chỉ tách đường dẫn theo dấu /, nên trên Windows tên vault thành cả đường dẫn ổ đĩa.
**Bài học:** Cache có thể đổi nội dung thư mục theo cách không ai nghĩ tới, nên đừng dùng thư mục cache để chứa dữ liệu kiểm thử. Tên thư mục trên Windows cần tách theo cả hai loại dấu phân cách.
**Artefact:** Danh sách các lần chạy CI đỏ và xanh (không có ID nhạy cảm).
