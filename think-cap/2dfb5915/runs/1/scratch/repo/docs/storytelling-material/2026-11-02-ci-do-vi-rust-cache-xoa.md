---
id: 2026-11-02-ci-do-vi-rust-cache-xoa
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1264", "claude:2dfb5915#L1364"]
hook: "Mã không đổi một dòng, vậy mà CI đỏ trên cả ba hệ điều hành"
tension: nho_ma_to
sides: ["Không đổi dòng mã nào", "Ba hệ điều hành đỏ cùng lúc"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# CI đỏ vì rust-cache xoá file: dump đặt trong thư mục cache

**Bối cảnh:** Bước parity ghi dump ra thư mục nằm trong target, và thư mục đó được cache.
**Chuyện gì xảy ra:** Swatinem/rust-cache xoá mọi file ngoài thư mục build và giữ lại thư mục rỗng. Lần chạy đầu ghi thư mục con, cache lưu thư mục rỗng không có manifest. Các lần sau cache khôi phục khớp chính xác, check thấy thư mục không rỗng nhưng không có manifest nên từ chối. Ba OS đỏ trong khi mã không đổi. Sửa: ghi dump ra RUNNER_TEMP. Chạy local không tái hiện vì không ai xoá target.
**Bài học:** Đừng đặt đầu ra cần giữ trong thư mục cache; CI đỏ có thể không liên quan đến code.
**Artefact:** Trích log CI, che đường dẫn.
