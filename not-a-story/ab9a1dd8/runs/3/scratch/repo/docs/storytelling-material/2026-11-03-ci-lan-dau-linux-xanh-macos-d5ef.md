---
id: 2026-11-03-ci-lan-dau-linux-xanh-macos-d5ef
code: M-MY6V
aliases: [M-MY6V]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2315", "claude:ab9a1dd8#L2338", "claude:ab9a1dd8#L2362", "claude:ab9a1dd8#L2513", "claude:ab9a1dd8#L2544"]
hook: "CI lần đầu: Linux xanh, macOS đỏ 2 test, Windows đỏ 38 test"
tension: tuong_ma_hoa_ra
sides: ["Linux xanh cả 3 bản Node, tưởng đã ổn", "macOS đỏ vì symlink /var, Windows đỏ 38 test viết riêng cho POSIX"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# CI lần đầu: Linux xanh, macOS đỏ vì /var là symlink, Windows có 38 test viết riêng cho POSIX

**Bối cảnh:** Push lên main lần đầu với 9 tổ hợp: Linux, macOS, Windows, mỗi OS với Node 20, 22, 24.
**Chuyện gì xảy ra:** Linux xanh cả 3 bản Node. macOS đỏ 2 test vì repo nằm sau symlink /var trỏ tới /private/var nên không tìm thấy transcript. Windows đỏ 38 test: test chèn đường dẫn thô vào JSON, kiểm quyền 0600, tách biến bằng dấu hai chấm, và dùng claude giả không chạy được. Sau hai vòng sửa, Windows còn 4 lỗi và macOS xanh.
**Bài học:** Chỉ chạy CI trên OS thật mới bắt được lỗi symlink và đường dẫn Windows. Máy Linux xanh không đủ để tin.
**Artefact:** Ảnh GitHub Actions có 9 ô xanh. Che tên repo nếu cần.
