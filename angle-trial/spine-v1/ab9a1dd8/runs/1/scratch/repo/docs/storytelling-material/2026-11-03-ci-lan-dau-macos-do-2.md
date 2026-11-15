---
id: 2026-11-03-ci-lan-dau-macos-do-2
date: 2026-11-03
repo: repo
status: raw
signals: [số trước sau, nguyên nhân bất ngờ]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2322", "claude:ab9a1dd8#L2334", "claude:ab9a1dd8#L2347", "claude:ab9a1dd8#L2359", "claude:ab9a1dd8#L2513", "claude:ab9a1dd8#L2535", "claude:ab9a1dd8#L2548"]
hook: "CI lần đầu: macOS đỏ 2 test, Windows đỏ 38"
tension: tuong_ma_hoa_ra
sides: ["Máy Linux xanh tưởng chạy được mọi nơi", "Windows đỏ 38 test vì giả định kiểu POSIX"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một công cụ dòng lệnh đọc transcript phiên làm việc với coding agent đang chuẩn bị gói phát hành đa nền tảng. Linux xanh cả ba bản Node ở lần CI đầu tiên, nhưng macOS đỏ 2 test và Windows đỏ 38 test. Xanh trên một hệ điều hành chưa nói gì về hai hệ còn lại, và chỉ chạy CI thật trên cả ba mới lộ ra chuyện này."
audience: dev viết test cho công cụ dòng lệnh đa nền tảng
spine_context: "Công cụ dòng lệnh đọc transcript phiên làm việc với coding agent, đang làm gói phát hành đa nền tảng (packaging-distribution)."
spine_context_lines: [profile, "claude:ab9a1dd8#L664"]
spine_want: "Hoàn tất plan packaging-distribution, gồm đẩy code lên GitHub để CI chạy lần đầu và kiểm nhánh Windows trên máy thật."
spine_want_lines: ["claude:ab9a1dd8#L664", "claude:ab9a1dd8#L2233"]
spine_obstacle: Test scan của macOS không tìm thấy phiên nào của repo; Windows đỏ 38 test.
spine_obstacle_lines: ["claude:ab9a1dd8#L2334", "claude:ab9a1dd8#L2362"]
spine_turn: "Linux xanh cả ba bản Node ở lần CI đầu; hoá ra macOS và Windows vẫn đỏ, nên xanh trên một hệ điều hành chưa đủ để kết luận cho các hệ còn lại."
spine_turn_lines: ["claude:ab9a1dd8#L2318", "claude:ab9a1dd8#L2334", "claude:ab9a1dd8#L2362"]
spine_action: "Nghi /var là symlink, đổi cách chuẩn hoá đường dẫn trong lib/repo.mjs rồi chạy lại test."
spine_action_lines: ["claude:ab9a1dd8#L2338", "claude:ab9a1dd8#L2532"]
spine_outcome: "Windows giảm từ 38 lỗi xuống 4; ở lần CI sau macOS xanh cả ba bản Node, Windows vẫn đỏ."
spine_outcome_lines: ["claude:ab9a1dd8#L2513", "claude:ab9a1dd8#L2544"]
spine_takeaway: Test chỉ chạy trên một hệ điều hành có thể mang giả định của hệ đó; chạy CI trên đúng các OS người dùng sẽ dùng mới lộ ra lỗi.
spine_takeaway_lines: ["claude:ab9a1dd8#L2362", "claude:ab9a1dd8#L2544"]
completeness: 7
---

# CI lần đầu: macOS đỏ 2 test, Windows đỏ 38 test

**Góc kể:** Một công cụ dòng lệnh đọc transcript phiên làm việc với coding agent đang chuẩn bị gói phát hành đa nền tảng. Linux xanh cả ba bản Node ở lần CI đầu tiên, nhưng macOS đỏ 2 test và Windows đỏ 38 test. Xanh trên một hệ điều hành chưa nói gì về hai hệ còn lại, và chỉ chạy CI thật trên cả ba mới lộ ra chuyện này.
**Bối cảnh:** Linux xanh cả ba bản Node ngay từ lần đầu. Hai hệ điều hành còn lại được chạy qua CI thật.
**Chuyện gì xảy ra:** macOS lỗi vì /var là symlink tới /private/var, nên không tìm thấy phiên của repo. Windows lỗi 38 test, phần lớn là test viết cho POSIX: chèn đường dẫn thô vào JSON, kiểm quyền 0600, tách bằng dấu hai chấm. Sau các sửa, Windows giảm từ 38 xuống 4 rồi về 0; macOS xanh cả ba bản Node.
**Bài học:** Test viết trên một OS sẽ mang giả định của OS đó. Chạy CI thật trên cả ba OS mới lộ ra điều này.
**Artefact:** Bảng 9 job CI (ảnh GitHub Actions). Che tên người dùng trong đường dẫn log.
