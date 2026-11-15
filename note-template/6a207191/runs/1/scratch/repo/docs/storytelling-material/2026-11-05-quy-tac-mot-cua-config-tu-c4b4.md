---
id: 2026-11-05-quy-tac-mot-cua-config-tu-c4b4
code: M-JZ0C
aliases: [M-JZ0C]
date: 2026-11-05
repo: repo
status: raw
signals: [dao_quyet_dinh, rang_buoc_thiet_ke]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:6a207191#L2255", "claude:6a207191#L2324", "claude:6a207191#L2333", "claude:6a207191#L2385", "claude:6a207191#L2393", "claude:6a207191#L2407"]
hook: "Quy tắc một cửa config đã có test, nhưng chưa người dùng nào chạm tới"
tension: tuong_ma_hoa_ra
sides: ["Quy tắc được chép thành chuẩn chung, có test", "Chưa có bản phát hành nên chưa chứng minh với người dùng thật"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: Dự án momentry vừa chốt quy tắc mọi cài đặt đổi qua `config`; người làm muốn kiểm tra skill chung đã có quy chuẩn này chưa.
spine_context_lines: ["claude:6a207191#L2255"]
spine_want: Biết skill cs-packaging-distribution đã có quy chuẩn 'một cửa config' chưa.
spine_want_lines: ["claude:6a207191#L2255"]
spine_obstacle: "Skill chỉ có các mảnh rời về config (CFG-04, UX-12, UX-14), thiếu quy tắc cấm cờ lẻ."
spine_obstacle_lines: ["claude:6a207191#L2324"]
spine_action: "Thêm CMD-22..24, nâng CFG-12 lên MUST, thêm tham chiếu momentry rồi gửi lên hub."
spine_action_lines: ["claude:6a207191#L2385", "claude:6a207191#L2407"]
spine_outcome: lint-guides qua với 215 quy tắc; check-references xác nhận mọi đường dẫn; bản gửi đang chờ duyệt.
spine_outcome_lines: ["claude:6a207191#L2385", "claude:6a207191#L2407"]
completeness: 5
---

# Quy tắc 'một cửa config' từ momentry được chép thành quy chuẩn chung

**Bối cảnh:** Dự án momentry vừa chốt quy tắc: mọi cài đặt, kể cả cài đặt riêng dự án, chỉ đổi qua `config`. Người dùng yêu cầu kiểm tra skill chung đã có chưa.
**Chuyện gì xảy ra:** Đối chiếu cho thấy skill chỉ có mảnh rời (CFG-04, UX-12, UX-14), thiếu quy tắc cấm cờ lẻ. Thêm ba rule CMD-22..24 và nâng CFG-12 lên MUST, đưa commit momentry vào references.md. Lưu ý: commit này chưa có bản phát hành nào, nên chỉ được coi là đã có test chứ chưa là đã chứng minh với người dùng.
**Bài học:** Một quy chuẩn chung chỉ đáng tin khi có ví dụ thật; đánh dấu rõ những gì mới có test và chưa được dùng thật.
**Artefact:** Mục '6. Config — one door for every setting' trong 07-command-surface.md (không chụp dữ liệu riêng).
**Góc người ngoài:** cách làm phổ biến là Hầu hết người ta ghi quy tắc vào README của dự án hoặc để trong đầu, không có ID quy tắc, không có liên kết về code mẫu và không có bước kiểm tra đường dẫn còn tồn tại; ở đây khác ở Phiên này đối chiếu quy tắc mới với những gì đã có, thêm đúng một chỗ định nghĩa, rồi chạy script kiểm tra cả cấu trúc lẫn đường dẫn tham chiếu. Người đọc sẽ muốn biết cách tránh việc một quy tắc nằm rải rác ở nhiều nơi.
