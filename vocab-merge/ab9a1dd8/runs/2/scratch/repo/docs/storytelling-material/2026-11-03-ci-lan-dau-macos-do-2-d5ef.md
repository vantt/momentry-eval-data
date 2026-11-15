---
id: 2026-11-03-ci-lan-dau-macos-do-2-d5ef
code: M-11Q8
aliases: [M-11Q8]
date: 2026-11-03
repo: repo
status: raw
signals: [số trước sau, nguyên nhân bất ngờ]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2322", "claude:ab9a1dd8#L2334", "claude:ab9a1dd8#L2347", "claude:ab9a1dd8#L2359", "claude:ab9a1dd8#L2513", "claude:ab9a1dd8#L2535", "claude:ab9a1dd8#L2548"]
hook: "CI đầu tiên: Windows đỏ 38 test, macOS đỏ 2"
tension: tuong_ma_hoa_ra
sides: ["test xanh trên máy Linux", "38 test đỏ trên Windows vì viết cho POSIX"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# CI lần đầu: macOS đỏ 2 test, Windows đỏ 38 test

**Bối cảnh:** Linux xanh cả ba bản Node ngay từ lần đầu. Hai hệ điều hành còn lại được chạy qua CI thật.
**Chuyện gì xảy ra:** macOS lỗi vì /var là symlink tới /private/var, nên không tìm thấy phiên của repo. Windows lỗi 38 test, phần lớn là test viết cho POSIX: chèn đường dẫn thô vào JSON, kiểm quyền 0600, tách bằng dấu hai chấm. Sau các sửa, Windows giảm từ 38 xuống 4 rồi về 0; macOS xanh cả ba bản Node.
**Bài học:** Test viết trên một OS sẽ mang giả định của OS đó. Chạy CI thật trên cả ba OS mới lộ ra điều này.
**Artefact:** Bảng 9 job CI (ảnh GitHub Actions). Che tên người dùng trong đường dẫn log.
