---
id: 2026-11-03-ci-chin-to-hop-lan-dau
date: 2026-11-03
repo: repo
status: raw
signals: ["2", "1"]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2315", "claude:ab9a1dd8#L2318", "claude:ab9a1dd8#L2362", "claude:ab9a1dd8#L2494", "claude:ab9a1dd8#L2513", "claude:ab9a1dd8#L2544", "claude:ab9a1dd8#L2810"]
hook: "CI lần đầu: Linux xanh, Windows đỏ 38 test"
tension: tuong_ma_hoa_ra
sides: ["Linux xanh, tưởng code ổn", "Windows đỏ 38 test vì test giả định POSIX"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# CI chín tổ hợp lần đầu: Linux xanh, macOS và Windows đỏ hàng loạt

**Bối cảnh:** Lần push đầu tiên, CI chạy ba hệ điều hành với ba bản Node.
**Chuyện gì xảy ra:** Linux xanh, macOS đỏ hai test, Windows đỏ 38 test. Số lỗi Windows xuống còn 4 sau lần sửa đầu, và về 0 khi test được viết lại không giả định POSIX. Nguyên nhân là test chèn đường dẫn thô vào JSON, kiểm quyền 0600, tách bằng dấu hai chấm, và claude giả không chạy được trên Windows.
**Bài học:** Test viết theo giả định POSIX sẽ đỏ trên Windows. CI ba hệ điều hành là cách duy nhất có máy thật để kiểm.
**Artefact:** Bảng chín job, xanh hoặc đỏ, theo từng tổ hợp hệ điều hành và Node.
