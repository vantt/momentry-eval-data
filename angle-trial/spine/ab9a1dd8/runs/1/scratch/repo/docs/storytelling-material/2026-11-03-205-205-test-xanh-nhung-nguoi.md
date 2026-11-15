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
angle: "Một công cụ dòng lệnh nhặt chất liệu kể chuyện từ phiên làm việc với coding agent, đang chuẩn bị đưa tới người ngoài dùng. Bộ test 205/205 xanh trên clone sạch dễ bị hiểu là đã sẵn sàng, nhưng khi chạy đúng quick start từ HOME trống, lệnh init --yes báo 'Unknown option' và người mới không qua nổi bước đầu. Chuyện đáng nghe vì test xanh chỉ chứng minh code chạy trong môi trường test, không chứng minh người dùng cài được; chỉ kiểm từ con số 0 mới lộ ra điều đó."
audience: dev làm công cụ CLI cần phân phối cho người khác
spine_context: "Một công cụ dòng lệnh nhặt chất liệu kể chuyện từ phiên làm việc với coding agent, đang chuẩn bị đưa tới người ngoài dùng."
spine_context_lines: [profile, "claude:ab9a1dd8#L42"]
spine_want: "Người mới cài và chạy được từ con số 0, không phải hỏi lại."
spine_want_lines: ["claude:ab9a1dd8#L42"]
spine_obstacle: "Lệnh init --yes báo 'Unknown option', nên người mới dừng ngay bước đầu."
spine_obstacle_lines: ["claude:ab9a1dd8#L232"]
spine_turn: Bộ test 205/205 xanh trên clone sạch bị coi là dấu hiệu đã sẵn sàng; hoá ra người mới không cài nổi.
spine_turn_lines: ["claude:ab9a1dd8#L170", "claude:ab9a1dd8#L232"]
spine_action: "Chạy các bước kiểm của skill trong HOME tạm, không đụng cấu hình thật."
spine_action_lines: ["claude:ab9a1dd8#L236"]
spine_outcome: "Lập plan 8 phase, 45 việc, ước khoảng 9 ngày công; chưa sửa dòng code nào."
spine_outcome_lines: ["claude:ab9a1dd8#L653"]
spine_takeaway: Test xanh không chứng minh người dùng cài được; chạy đúng quick start từ HOME trống trước khi tin bộ test.
spine_takeaway_lines: ["claude:ab9a1dd8#L170", "claude:ab9a1dd8#L232"]
completeness: 7
---

# 205/205 test xanh nhưng người mới không cài nổi

**Góc kể:** Một công cụ dòng lệnh nhặt chất liệu kể chuyện từ phiên làm việc với coding agent, đang chuẩn bị đưa tới người ngoài dùng. Bộ test 205/205 xanh trên clone sạch dễ bị hiểu là đã sẵn sàng, nhưng khi chạy đúng quick start từ HOME trống, lệnh init --yes báo 'Unknown option' và người mới không qua nổi bước đầu. Chuyện đáng nghe vì test xanh chỉ chứng minh code chạy trong môi trường test, không chứng minh người dùng cài được; chỉ kiểm từ con số 0 mới lộ ra điều đó.
**Bối cảnh:** Dự án CLI đã có bộ test lớn và lõi chạy ổn. Agent được yêu cầu audit phần đóng gói và cài đặt theo một skill chuẩn.
**Chuyện gì xảy ra:** Trên clone sạch, 205/205 test qua. Nhưng README không có bước lấy code, không có version, install, update hay uninstall. Lệnh `init --yes --json` báo 'Unknown option'. Agent lập plan 8 phase với 45 việc, ước khoảng 9 ngày công.
**Bài học:** Test xanh không chứng minh người dùng cài được. Hãy chạy đúng quick start từ HOME trống trước khi tin vào bộ test.
**Artefact:** Bảng checklist đóng gói (ID rule, MUST/SHOULD, trạng thái). Che đường dẫn máy và tên người dùng.
