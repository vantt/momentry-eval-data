---
id: 2026-11-02-may-windows-thu-ra-ba-loi-3c6e
code: M-48ZD
aliases: [M-48ZD]
date: 2026-11-02
repo: repo
status: raw
signals: [khac, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L3233", "claude:2dfb5915#L3242", "claude:2dfb5915#L3277"]
hook: "Máy Windows thật lộ ba lỗi mà test Linux không thấy"
tension: tuong_ma_hoa_ra
sides: ["Harness xanh trên máy dev", "Windows lộ ba lỗi: đường dẫn JSON, UTF-8, và cờ -I ẩn user site"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "Một công cụ dòng lệnh để hỏi Claude Desktop về graph của vault Obsidian, đang thay lõi bằng Rust để chuẩn bị bản rc.2."
spine_context_lines: [profile]
spine_want: Đưa bản rc.2 cho người dùng Windows cài thử.
spine_want_lines: ["claude:2dfb5915#L3219"]
spine_obstacle: "Máy Windows thử lộ ba lỗi: che đường dẫn JSON, in tiếng Việt qua pipe sập, và probe không thấy PyYAML cài bằng --user."
spine_obstacle_lines: ["claude:2dfb5915#L3242"]
spine_action: "Sửa ba lỗi, cập nhật bản bàn giao và đưa báo cáo Windows vào main."
spine_action_lines: ["claude:2dfb5915#L3242"]
spine_outcome: "CI trên main xanh trên Linux, macOS và Windows sau khi job macOS ARM chờ runner được chạy lại."
spine_outcome_lines: ["claude:2dfb5915#L3277"]
spine_takeaway: Phase 10 vẫn cần chạy lại bộ so khớp riêng trên Windows để xác nhận.
spine_takeaway_lines: ["claude:2dfb5915#L3242"]
completeness: 6
---

# Máy Windows thử ra ba lỗi harness: đường dẫn JSON, UTF-8 khi pipe, và -I ẩn user site

**Bối cảnh:** Người dùng chạy phần thử trên một máy Windows sạch, gồm cả việc chạy harness với vault thật.
**Chuyện gì xảy ra:** Ba lỗi: Scrub không che đường dẫn Windows dạng escape trong JSON nên CLI lệch 2 mục; in tiếng Việt qua pipe khiến script sập với cp1252; và probe chạy python -I làm ẩn user site, nên không thấy PyYAML cài bằng --user. Fix bằng -E -P, giữ được bảo vệ không import code từ vault.
**Bài học:** Thử trên máy thật có đường dẫn, mã hoá và môi trường Python khác bắt được lỗi mà CI Linux không thấy.
**Artefact:** Báo cáo thử Windows (chụp phần tóm tắt, che đường dẫn).
