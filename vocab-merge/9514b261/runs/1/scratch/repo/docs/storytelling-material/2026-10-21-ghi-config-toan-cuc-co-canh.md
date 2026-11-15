---
id: 2026-10-21-ghi-config-toan-cuc-co-canh
date: 2026-10-21
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L2375", "claude:9514b261#L2438", "claude:9514b261#L2492", "claude:9514b261#L3620"]
hook: "Doctor báo năm check PASS, nhưng các workspace chạy release cũ chưa ai kiểm"
tension: tuong_ma_hoa_ra
sides: ["Sao lưu config, chỉ ghi một khoá, doctor PASS cả năm check", "Khoá mới có thể làm hỏng máy chạy release cũ, việc kiểm còn để lại"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Ghi config toàn cục có cảnh báo: khoá mới có thể làm hỏng máy chạy release cũ

**Bối cảnh:** Hướng dẫn của một máy khác cảnh báo rằng thêm khoá mới vào config toàn cục từng làm hỏng workspace chạy release cũ.
**Chuyện gì xảy ra:** Agent sao lưu config, chỉ ghi khoá runner.llmAccounts và giữ nguyên các khoá khác. Doctor báo năm check về tài khoản đều PASS. Việc kiểm các workspace khác chạy release cũ thì chưa làm, và được để lại như việc còn lại.
**Bài học:** Đọc cảnh báo tương thích của bản cũ trước khi thêm khoá vào config dùng chung, rồi kiểm các máy còn lại.
