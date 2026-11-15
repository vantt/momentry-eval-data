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
hook: "Cache làm CI đỏ cả 3 OS, chạy máy mình thì vẫn xanh"
tension: giup_ma_hai
sides: ["Cache được bật để CI chạy nhanh hơn", "Cache xoá file dump nên CI đỏ cả ba hệ điều hành"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# CI đỏ trên cả ba OS vì cache xoá file dump, và tên vault trên Windows bị sai

**Bối cảnh:** Bước parity của CI dùng rust-cache để lưu thư mục target.
**Chuyện gì xảy ra:** Rust-cache lưu target nhưng xoá mọi file ngoài thư mục build của cargo, chỉ giữ lại các thư mục rỗng. Từ lần chạy sau, cache được khôi phục khớp chính xác nên bước check thấy thư mục dump không rỗng mà không có manifest, từ chối ghi đè và thoát mã 2 trên cả ba OS. Chạy cục bộ thì không lỗi vì không ai xoá target. Ở lỗi thứ hai, hàm basename chỉ tách đường dẫn theo dấu /, nên trên Windows tên vault thành cả đường dẫn ổ đĩa.
**Bài học:** Cache có thể đổi nội dung thư mục theo cách không ai nghĩ tới, nên đừng dùng thư mục cache để chứa dữ liệu kiểm thử. Tên thư mục trên Windows cần tách theo cả hai loại dấu phân cách.
**Artefact:** Danh sách các lần chạy CI đỏ và xanh (không có ID nhạy cảm).
