---
id: 2026-11-02-debounce-watcher-5-giay-tieu-chi-40f9
code: M-8Q1A
aliases: [M-8Q1A]
date: 2026-11-02
repo: repo
status: raw
signals: [đảo quyết định có lý do, ràng buộc định hình thiết kế]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L1614", "claude:c4caee3c#L1615", "claude:c4caee3c#L1923", "claude:c4caee3c#L1926"]
hook: "Tiêu chí 1 giây không hạ: debounce 5 giây thành biến môi trường"
tension: chon_mot_mat_mot
sides: ["giữ nguyên tiêu chí 1 giây", "mặc định vẫn 5 giây, client tự đặt 250 ms"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Debounce watcher 5 giây: tiêu chí 1 giây không hạ, đưa thành biến môi trường

**Bối cảnh:** Client sự kiện cần thấy file được index trong 1 giây, nhưng watcher upstream chờ 5 giây.
**Chuyện gì xảy ra:** Lead giữ quy tắc không hạ ngưỡng. Agent thêm OBSIDIAN_WATCH_DEBOUNCE_MS, mặc định vẫn 5 giây, client đặt 250 ms. Test chứng minh sự kiện đến trong dưới 1 giây.
**Bài học:** Khi tiêu chí và mặc định mâu thuẫn, tách thành cấu hình thay vì đổi giá trị gốc.
