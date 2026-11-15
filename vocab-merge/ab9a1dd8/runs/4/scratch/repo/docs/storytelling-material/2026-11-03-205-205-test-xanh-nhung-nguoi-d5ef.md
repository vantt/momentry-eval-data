---
id: 2026-11-03-205-205-test-xanh-nhung-nguoi-d5ef
code: M-AAYD
aliases: [M-AAYD]
date: 2026-11-03
repo: repo
status: raw
signals: [số trước sau, nguyên nhân bất ngờ]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L170", "claude:ab9a1dd8#L232", "claude:ab9a1dd8#L236", "claude:ab9a1dd8#L653"]
hook: "205/205 test xanh, mà người mới không cài nổi"
tension: tuong_ma_hoa_ra
sides: ["205/205 test xanh trên clone sạch", "README thiếu cả bước lấy code và init --yes --json báo lỗi"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# 205/205 test xanh nhưng người mới không cài nổi

**Bối cảnh:** Dự án CLI đã có bộ test lớn và lõi chạy ổn. Agent được yêu cầu audit phần đóng gói và cài đặt theo một skill chuẩn.
**Chuyện gì xảy ra:** Trên clone sạch, 205/205 test qua. Nhưng README không có bước lấy code, không có version, install, update hay uninstall. Lệnh `init --yes --json` báo 'Unknown option'. Agent lập plan 8 phase với 45 việc, ước khoảng 9 ngày công.
**Bài học:** Test xanh không chứng minh người dùng cài được. Hãy chạy đúng quick start từ HOME trống trước khi tin vào bộ test.
**Artefact:** Bảng checklist đóng gói (ID rule, MUST/SHOULD, trạng thái). Che đường dẫn máy và tên người dùng.
