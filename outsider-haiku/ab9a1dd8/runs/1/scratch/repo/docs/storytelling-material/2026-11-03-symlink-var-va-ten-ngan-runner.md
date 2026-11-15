---
id: 2026-11-03-symlink-var-va-ten-ngan-runner
date: 2026-11-03
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2338", "claude:ab9a1dd8#L2464", "claude:ab9a1dd8#L2532", "claude:ab9a1dd8#L2580", "claude:ab9a1dd8#L2586"]
hook: "Test không thấy phiên nào vì /var và RUNNER~1 là cùng một đường dẫn"
tension: nho_ma_to
sides: ["cùng một thư mục, hai cách viết đường dẫn", "test không thấy phiên transcript nào"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Symlink /var và tên ngắn RUNNER~1 làm mất phiên transcript

**Bối cảnh:** momentry tìm transcript Claude theo đường dẫn repo đã mã hoá. macOS có /var là symlink tới /private/var; runner Windows có đường dẫn ngắn kiểu 8.3.
**Chuyện gì xảy ra:** Test scan không thấy phiên trên macOS vì hai dạng đường dẫn không khớp nhau. Trên Windows, tên ngắn RUNNER~1 và chữ hoa của ổ đĩa làm so khớp thất bại. Sửa xong thì so khớp cả đường dẫn thật lẫn dạng đã mở rộng, và không phân biệt hoa thường trên Windows.
**Bài học:** Chuẩn hoá đường dẫn bằng realpath và dạng native trước khi so; đừng so chuỗi thô.
**Artefact:** Dòng test không ok trong log CI, che đường dẫn runner.
