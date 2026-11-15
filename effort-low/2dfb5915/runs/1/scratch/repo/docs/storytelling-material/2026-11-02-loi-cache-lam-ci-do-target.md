---
id: 2026-11-02-loi-cache-lam-ci-do-target
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1264", "claude:2dfb5915#L1272", "claude:2dfb5915#L1283", "claude:2dfb5915#L1291", "claude:2dfb5915#L1304"]
hook: "CI đỏ vì công cụ cache dọn mất thư mục dump, chỉ còn cái vỏ rỗng"
tension: giup_ma_hai
sides: ["Cache để chạy nhanh hơn và ổn định hơn", "Cache xoá file ngoài thư mục build, giữ lại thư mục rỗng, CI đỏ lặp lại"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Lỗi cache làm CI đỏ: target/ bị rust-cache xoá file ngoài thư mục build

**Bối cảnh:** Bước so khớp parity trên cả ba OS đỏ từ một lần chạy CI, dù code không đổi.
**Chuyện gì xảy ra:** Swatinem/rust-cache chỉ giữ thư mục build của cargo, xoá file khác và giữ lại thư mục rỗng. Lần chạy đầu ghi cache với thư mục dump rỗng, các lần sau khôi phục đúng cache đó và kiểm tra thấy thư mục không có manifest. Sửa bằng cách ghi dump ra ngoài target/.
**Bài học:** Đừng ghi artefact sinh ra vào thư mục mà cache tool quản lý; cache khôi phục thành công vẫn có thể hỏng.
**Artefact:** Đoạn log CI đỏ và diff dòng sửa ci.yml.
