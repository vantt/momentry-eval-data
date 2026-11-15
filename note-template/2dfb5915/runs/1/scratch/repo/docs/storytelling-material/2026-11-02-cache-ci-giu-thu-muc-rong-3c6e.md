---
id: 2026-11-02-cache-ci-giu-thu-muc-rong-3c6e
code: M-858R
aliases: [M-858R]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1264", "claude:2dfb5915#L1283", "claude:2dfb5915#L1291"]
hook: "Cache giữ lại một thư mục rỗng, CI đỏ cả ba nền"
tension: giup_ma_hai
sides: ["Cache để chạy nhanh và ổn định hơn", "Nó giữ thư mục rỗng làm CI sập từ lần chạy kế tiếp"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Cache CI giữ thư mục rỗng, CI đỏ từ lần chạy kế tiếp

**Bối cảnh:** Bước kiểm bộ so khớp dump ra thư mục nằm trong target của cargo, được cache giữa các lần chạy CI.
**Chuyện gì xảy ra:** Action cache xoá mọi file ngoài thư mục build và giữ lại thư mục rỗng. Lần chạy đầu lưu cache hỏng; các lần sau khôi phục đúng khớp nên bước kiểm thấy thư mục có sẵn mà không có manifest, và sập cả ba nền. Local vẫn xanh vì target không bao giờ bị dọn. Sửa bằng cách xuất dump ra thư mục tạm ngoài cache.
**Bài học:** Đừng để đầu ra của bước kiểm nằm trong thư mục cache.
