---
id: 2026-11-03-ci-lan-dau-windows-do-38-d5ef
code: M-KYRK
aliases: [M-KYRK]
date: 2026-11-03
repo: repo
status: raw
signals: [khac, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2315", "claude:ab9a1dd8#L2356", "claude:ab9a1dd8#L2362", "claude:ab9a1dd8#L2424", "claude:ab9a1dd8#L2447", "claude:ab9a1dd8#L2513", "claude:ab9a1dd8#L2548"]
hook: "Linux xanh cả ba bản Node, Windows đỏ 38 test"
tension: tuong_ma_hoa_ra
sides: ["Test xanh trên Linux, tưởng chạy mọi nơi", "Windows đỏ 38 test vì test ngầm giả định POSIX"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# CI lần đầu: Windows đỏ 38 test vì test viết cho POSIX

**Bối cảnh:** Lần chạy CI đầu tiên trên GitHub, ma trận ba hệ điều hành nhân ba bản Node.
**Chuyện gì xảy ra:** Linux xanh cả ba bản Node, macOS đỏ 2 test, Windows đỏ 38 test. Phần lớn lỗi Windows là test giả định POSIX: chèn đường dẫn thô vào JSON, kiểm quyền 0600, tách PATH bằng dấu hai chấm, và claude giả không chạy được. Sau sửa, Windows còn 4 lỗi, macOS còn 2 lỗi, do repo nằm sau symlink /var trỏ tới /private/var.
**Bài học:** Đường dẫn và quyền file là chỗ CI nhiều nền tảng bắt lỗi trước máy cá nhân; chạy ba hệ điều hành ngay từ commit đầu.
**Artefact:** Ảnh ma trận CI chín ô, ba hệ điều hành nhân Node 20, 22, 24, lúc xanh.
