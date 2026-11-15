---
id: 2026-11-02-ci-do-vi-cache-xoa-file
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1264", "claude:2dfb5915#L1283", "claude:2dfb5915#L1291", "claude:2dfb5915#L1364"]
hook: "Cache giữ thư mục rỗng, CI đỏ dù dump đã ghi"
tension: cam_ma_van_lot
sides: ["cache được khôi phục khớp chính xác", "file bị xoá còn thư mục rỗng, bước so khớp từ chối chạy"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# CI đỏ vì cache xoá file nhưng giữ thư mục rỗng

**Bối cảnh:** Bước so khớp parity đỏ trên cả ba OS từ một lần đẩy trở đi, dù code không đổi ở đó.
**Chuyện gì xảy ra:** Rust-cache chỉ lưu thư mục target. Nó xoá file nằm ngoài các thư mục build nhưng vẫn giữ thư mục rỗng. Một lần chạy đã lưu cache với dump chỉ còn thư mục rỗng. Các lần sau cache được khôi phục khớp chính xác, và bước so khớp từ chối ghi vào thư mục không có manifest. Gốc lỗi là ghi dump vào chỗ cache quản lý.
**Bài học:** Đừng ghi output vào thư mục mà cache của CI quản lý. Đưa output ra thư mục tạm của runner.
**Artefact:** Sơ đồ ba bước: ghi dump, lưu cache, khôi phục ở lần sau.
