---
id: 2026-11-03-ci-lan-dau-linux-xanh-macos-d5ef
code: M-MY6V
aliases: [M-MY6V]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2315", "claude:ab9a1dd8#L2338", "claude:ab9a1dd8#L2362", "claude:ab9a1dd8#L2513", "claude:ab9a1dd8#L2544"]
hook: "Linux xanh cả 3 bản, Windows đỏ 38 test"
tension: tuong_ma_hoa_ra
sides: ["Linux xanh toàn bộ, tưởng đã ổn", "macOS đỏ 2 test, Windows đỏ 38 test"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Momentry là công cụ nhặt chuyện đáng kể từ phiên làm việc với coding agent, và người làm đang chuẩn bị hoàn tất bản v2 bằng lần chạy CI đầu tiên. Linux xanh được xem là đủ, nhưng macOS đỏ vì đường dẫn /var là symlink, còn Windows đỏ 38 test viết riêng cho POSIX. Ai chỉ thử trên một hệ điều hành có thể tin nhầm rằng code đã chạy được ở mọi nơi."
audience: dev viết test cho công cụ đa nền tảng
spine_context: "Momentry nhặt những chuyện đáng kể từ phiên làm việc với coding agent, và người làm đang hoàn tất bản v2 với kế hoạch 45 việc."
spine_context_lines: [profile, "claude:ab9a1dd8#L2233"]
spine_want: "Hoàn tất plan, gồm đẩy code lên GitHub để CI chạy lần đầu trên các tổ hợp OS và Node."
spine_want_lines: ["claude:ab9a1dd8#L2233"]
spine_obstacle: "Lần chạy CI đầu tiên: Linux xanh, macOS và Windows đỏ, Windows có 38 test lỗi."
spine_obstacle_lines: ["claude:ab9a1dd8#L2318", "claude:ab9a1dd8#L2362"]
spine_turn: "Linux xanh được xem là đủ để tin; hoá ra macOS đỏ vì /var là symlink tới /private/var, còn Windows đỏ vì các test viết riêng cho POSIX."
spine_turn_lines: ["claude:ab9a1dd8#L2318", "claude:ab9a1dd8#L2338"]
spine_action: "Đọc log lỗi của CI, sửa qua hai vòng và đẩy lại mỗi lần."
spine_action_lines: ["claude:ab9a1dd8#L2497", "claude:ab9a1dd8#L2513"]
spine_outcome: macOS xanh cả 3 bản Node; Windows còn 4 lỗi sau vòng sửa thứ hai.
spine_outcome_lines: ["claude:ab9a1dd8#L2513", "claude:ab9a1dd8#L2544"]
spine_takeaway: Chỉ CI chạy trên hệ điều hành thật mới bắt được lỗi symlink và đường dẫn Windows; Linux xanh không đủ để tin.
spine_takeaway_lines: ["claude:ab9a1dd8#L2338", "claude:ab9a1dd8#L2513"]
completeness: 7
---

# CI lần đầu: Linux xanh, macOS đỏ vì /var là symlink, Windows có 38 test viết riêng cho POSIX

**Góc kể:** Momentry là công cụ nhặt chuyện đáng kể từ phiên làm việc với coding agent, và người làm đang chuẩn bị hoàn tất bản v2 bằng lần chạy CI đầu tiên. Linux xanh được xem là đủ, nhưng macOS đỏ vì đường dẫn /var là symlink, còn Windows đỏ 38 test viết riêng cho POSIX. Ai chỉ thử trên một hệ điều hành có thể tin nhầm rằng code đã chạy được ở mọi nơi.
**Bối cảnh:** Push lên main lần đầu với 9 tổ hợp: Linux, macOS, Windows, mỗi OS với Node 20, 22, 24.
**Chuyện gì xảy ra:** Linux xanh cả 3 bản Node. macOS đỏ 2 test vì repo nằm sau symlink /var trỏ tới /private/var nên không tìm thấy transcript. Windows đỏ 38 test: test chèn đường dẫn thô vào JSON, kiểm quyền 0600, tách biến bằng dấu hai chấm, và dùng claude giả không chạy được. Sau hai vòng sửa, Windows còn 4 lỗi và macOS xanh.
**Bài học:** Chỉ chạy CI trên OS thật mới bắt được lỗi symlink và đường dẫn Windows. Máy Linux xanh không đủ để tin.
**Artefact:** Ảnh GitHub Actions có 9 ô xanh. Che tên repo nếu cần.
