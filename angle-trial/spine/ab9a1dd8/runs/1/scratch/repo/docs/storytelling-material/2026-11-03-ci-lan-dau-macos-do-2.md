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
angle: "Một công cụ dòng lệnh nhặt chất liệu kể chuyện từ phiên làm việc với coding agent đang hoàn tất plan đóng gói, với mục tiêu CI xanh trên cả ba hệ điều hành. Linux xanh từ đầu nên tưởng vậy là ổn; khi CI thật chạy, macOS đỏ ở một test và Windows đỏ 38 test, vì test được viết theo giả định của OS đang dùng. Tới lần chạy đang xem, macOS đã xanh, Windows vẫn đỏ. Ai viết test cho CLI đa nền tảng nên chạy CI trên mọi OS sớm."
audience: dev viết test cho công cụ CLI đa nền tảng
spine_context: "Một công cụ dòng lệnh nhặt chất liệu kể chuyện từ phiên làm việc với coding agent, đang hoàn tất plan đóng gói và phân phối."
spine_context_lines: [profile, "claude:ab9a1dd8#L664"]
spine_want: "Hoàn tất plan 45 việc, với CI xanh trên cả ba hệ điều hành."
spine_want_lines: ["claude:ab9a1dd8#L664", "claude:ab9a1dd8#L2233"]
spine_obstacle: "CI chạy lần đầu: macOS đỏ ở test scan, Windows đỏ 38 test."
spine_obstacle_lines: ["claude:ab9a1dd8#L2334", "claude:ab9a1dd8#L2362"]
spine_turn: Tưởng máy Linux xanh là chạy được mọi nơi; hoá ra test mang giả định của OS đang dùng và sập trên hai OS còn lại.
spine_turn_lines: ["claude:ab9a1dd8#L2318", "claude:ab9a1dd8#L2362"]
spine_action: "Sửa cách chuẩn hoá đường dẫn trong lib/repo.mjs, rồi đẩy lên GitHub để CI chạy thật."
spine_action_lines: ["claude:ab9a1dd8#L2532", "claude:ab9a1dd8#L2538"]
spine_outcome: "macOS xanh cả ba bản Node; Windows vẫn đỏ ở lần chạy sau, plan còn 43/45."
spine_outcome_lines: ["claude:ab9a1dd8#L2233", "claude:ab9a1dd8#L2544"]
spine_takeaway: Test viết trên một OS mang giả định của OS đó; chạy CI thật trên cả ba OS sớm mới lộ ra.
spine_takeaway_lines: ["claude:ab9a1dd8#L2318", "claude:ab9a1dd8#L2529"]
completeness: 7
---

# CI lần đầu: macOS đỏ 2 test, Windows đỏ 38 test

**Góc kể:** Một công cụ dòng lệnh nhặt chất liệu kể chuyện từ phiên làm việc với coding agent đang hoàn tất plan đóng gói, với mục tiêu CI xanh trên cả ba hệ điều hành. Linux xanh từ đầu nên tưởng vậy là ổn; khi CI thật chạy, macOS đỏ ở một test và Windows đỏ 38 test, vì test được viết theo giả định của OS đang dùng. Tới lần chạy đang xem, macOS đã xanh, Windows vẫn đỏ. Ai viết test cho CLI đa nền tảng nên chạy CI trên mọi OS sớm.
**Bối cảnh:** Linux xanh cả ba bản Node ngay từ lần đầu. Hai hệ điều hành còn lại được chạy qua CI thật.
**Chuyện gì xảy ra:** macOS lỗi vì /var là symlink tới /private/var, nên không tìm thấy phiên của repo. Windows lỗi 38 test, phần lớn là test viết cho POSIX: chèn đường dẫn thô vào JSON, kiểm quyền 0600, tách bằng dấu hai chấm. Sau các sửa, Windows giảm từ 38 xuống 4 rồi về 0; macOS xanh cả ba bản Node.
**Bài học:** Test viết trên một OS sẽ mang giả định của OS đó. Chạy CI thật trên cả ba OS mới lộ ra điều này.
**Artefact:** Bảng 9 job CI (ảnh GitHub Actions). Che tên người dùng trong đường dẫn log.
