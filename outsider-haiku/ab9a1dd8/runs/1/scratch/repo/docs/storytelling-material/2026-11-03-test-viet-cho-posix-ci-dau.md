---
id: 2026-11-03-test-viet-cho-posix-ci-dau
date: 2026-11-03
repo: repo
status: raw
signals: [số trước/sau, nguyên nhân bất ngờ]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2322", "claude:ab9a1dd8#L2359", "claude:ab9a1dd8#L2362", "claude:ab9a1dd8#L2513", "claude:ab9a1dd8#L2548", "claude:ab9a1dd8#L2580", "claude:ab9a1dd8#L2810"]
hook: "Test viết cho POSIX: CI đầu tiên Windows đỏ 38 test, macOS đỏ 2"
tension: tuong_ma_hoa_ra
sides: ["test xanh trên máy POSIX", "Windows đỏ 38, macOS đỏ 2"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Test viết cho POSIX: CI đầu tiên Windows đỏ 38 test, macOS đỏ 2

**Bối cảnh:** Ma trận CI gồm 9 job cho ba hệ điều hành và Node 20, 22, 24. Linux xanh ngay, Windows và macOS đỏ.
**Chuyện gì xảy ra:** Phần lớn lỗi Windows nằm ở test giả định POSIX: chèn đường dẫn thô vào JSON, kiểm quyền 0600, tách biến bằng dấu hai chấm, và claude giả không chạy được trên Windows. Sau một lượt sửa, Windows còn 4 lỗi và macOS còn 2. Lần chạy cuối trên Windows: 231 pass, 0 fail.
**Bài học:** Đưa test vào CI đa nền tảng sớm; lỗi nằm ở test nhiều hơn ở code.
**Artefact:** Ma trận CI 9 job xanh.
