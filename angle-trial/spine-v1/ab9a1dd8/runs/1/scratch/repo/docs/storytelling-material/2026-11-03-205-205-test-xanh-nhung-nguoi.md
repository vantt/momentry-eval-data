---
id: 2026-11-03-205-205-test-xanh-nhung-nguoi
date: 2026-11-03
repo: repo
status: raw
signals: [số trước sau, nguyên nhân bất ngờ]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L170", "claude:ab9a1dd8#L232", "claude:ab9a1dd8#L236", "claude:ab9a1dd8#L653"]
hook: "205/205 test xanh, nhưng người mới không cài nổi"
tension: tuong_ma_hoa_ra
sides: ["205/205 test đều qua trên clone sạch", "README thiếu cả bước lấy code và init --yes --json báo lỗi"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: Một công cụ dòng lệnh đọc transcript phiên làm việc với coding agent và nhặt ra khoảnh khắc đáng kể làm chất liệu kể chuyện; đang chuẩn bị để người dùng cài và dùng được.
spine_context_lines: [profile]
spine_want: Muốn người mới đi từ con số 0 tới lần chạy đầu thành công qua một lệnh cài đặt.
spine_want_lines: ["claude:ab9a1dd8#L42"]
spine_obstacle: Lệnh init --yes --json báo Unknown option '--yes' khi chạy từ thư mục tạm.
spine_obstacle_lines: ["claude:ab9a1dd8#L232"]
spine_action: "Lập plan phân phối 8 phase, 45 việc; chưa sửa dòng code nào."
spine_action_lines: ["claude:ab9a1dd8#L653"]
spine_outcome: Plan đã qua ak plan validate.
spine_outcome_lines: ["claude:ab9a1dd8#L653"]
spine_takeaway: Test xanh không cho biết người mới cài được; hãy chạy đúng quick start từ thư mục trống để biết.
spine_takeaway_lines: ["claude:ab9a1dd8#L170", "claude:ab9a1dd8#L232"]
completeness: 6
---

# 205/205 test xanh nhưng người mới không cài nổi

**Bối cảnh:** Dự án CLI đã có bộ test lớn và lõi chạy ổn. Agent được yêu cầu audit phần đóng gói và cài đặt theo một skill chuẩn.
**Chuyện gì xảy ra:** Trên clone sạch, 205/205 test qua. Nhưng README không có bước lấy code, không có version, install, update hay uninstall. Lệnh `init --yes --json` báo 'Unknown option'. Agent lập plan 8 phase với 45 việc, ước khoảng 9 ngày công.
**Bài học:** Test xanh không chứng minh người dùng cài được. Hãy chạy đúng quick start từ HOME trống trước khi tin vào bộ test.
**Artefact:** Bảng checklist đóng gói (ID rule, MUST/SHOULD, trạng thái). Che đường dẫn máy và tên người dùng.
