---
id: 2026-11-03-ci-lan-dau-linux-xanh-macos-d5ef
code: M-MY6V
aliases: [M-MY6V]
date: 2026-11-03
repo: repo
status: raw
signals: [so_truoc_so_sau, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:ab9a1dd8#L2315", "claude:ab9a1dd8#L2334", "claude:ab9a1dd8#L2362", "claude:ab9a1dd8#L2497", "claude:ab9a1dd8#L2513", "claude:ab9a1dd8#L2544", "claude:ab9a1dd8#L2810"]
hook: "Linux xanh hết, Windows đỏ 38 test: test nào cũng tưởng mình là POSIX"
tension: tuong_ma_hoa_ra
sides: ["Linux xanh nên tưởng test ổn", "Windows đỏ 38 test vì giả định POSIX"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Công cụ đọc phiên làm việc với coding agent đang chuẩn bị phát hành và chạy CI lần đầu trên GitHub. Linux xanh nên tưởng test ổn, nhưng khi chạy trên Windows thì đỏ 38 test vì test viết giả định kiểu POSIX, còn macOS thì scan không thấy phiên vì /var là symlink. Ai viết test cho công cụ dòng lệnh đều nên đưa CI đa nền tảng vào sớm, vì máy mình xanh không có nghĩa là hệ điều hành khác cũng xanh."
audience: dev viết test cho công cụ dòng lệnh đa nền tảng
spine_context: "Công cụ đọc transcript các phiên làm việc với coding agent để nhặt ra chuyện đáng kể, đang chuẩn bị đóng gói và phát hành, bước tiếp theo là push lên GitHub để CI chạy lần đầu."
spine_context_lines: [profile, "claude:ab9a1dd8#L2233"]
spine_want: Muốn CI chạy lần đầu và xanh trên các nền tảng trước khi phát hành.
spine_want_lines: ["claude:ab9a1dd8#L2233"]
spine_obstacle: Windows đỏ 38 test ở lần chạy đầu.
spine_obstacle_lines: ["claude:ab9a1dd8#L2362"]
spine_turn: "Tưởng test xanh trên Linux nghĩa là chạy đúng; hoá ra test viết giả định POSIX, Windows đỏ 38 test, còn macOS scan không thấy phiên vì /var là symlink."
spine_turn_lines: ["claude:ab9a1dd8#L2338", "claude:ab9a1dd8#L2362"]
spine_action: "Đọc log từng dòng not ok, sửa các giả định theo hệ điều hành rồi đẩy lại để CI chạy tiếp."
spine_action_lines: ["claude:ab9a1dd8#L2513", "claude:ab9a1dd8#L2538"]
spine_outcome: macOS xanh cả 3 bản Node; Windows còn 231 pass và 0 fail ở lần chạy cuối.
spine_outcome_lines: ["claude:ab9a1dd8#L2544", "claude:ab9a1dd8#L2810"]
spine_takeaway: Test viết cho một hệ điều hành dễ hỏng ở hệ khác; đưa CI đa nền tảng vào sớm và đọc log lỗi từng test để tìm nguyên nhân.
spine_takeaway_lines: ["claude:ab9a1dd8#L2362", "claude:ab9a1dd8#L2544"]
completeness: 7
---

# CI lần đầu: Linux xanh, macOS đỏ 2 test, Windows đỏ 38 test; test viết giả định POSIX

**Góc kể:** Công cụ đọc phiên làm việc với coding agent đang chuẩn bị phát hành và chạy CI lần đầu trên GitHub. Linux xanh nên tưởng test ổn, nhưng khi chạy trên Windows thì đỏ 38 test vì test viết giả định kiểu POSIX, còn macOS thì scan không thấy phiên vì /var là symlink. Ai viết test cho công cụ dòng lệnh đều nên đưa CI đa nền tảng vào sớm, vì máy mình xanh không có nghĩa là hệ điều hành khác cũng xanh.
**Bối cảnh:** Push lên main lần đầu để CI chạy trên Linux, macOS và Windows với Node 20, 22, 24.
**Chuyện gì xảy ra:** Lần 1: Windows có 38 test lỗi. Lần 2: Windows còn 4, macOS 2; scan không thấy phiên vì /var là symlink tới /private/var trên macOS. Sau các sửa, macOS xanh cả 3 bản Node. Lần cuối 9/9 xanh, Windows 231 pass và 0 fail. Trước đó, PowerShell 5.1 làm hỏng JSON truyền cho chương trình ngoài, nên bước config set JSON được đổi sang privacy-add trên Windows.
**Bài học:** Test viết cho một hệ điều hành dễ hỏng ở hệ khác theo các kiểu quen thuộc: symlink /var, tên 8.3, dấu nháy trong JSON. Đưa CI đa nền tảng vào sớm.
**Artefact:** Ảnh trang CI 9 job xanh (che tên runner nếu có).
**Góc người ngoài:** cách làm phổ biến là Dev một mình thường chỉ chạy test trên máy mình, thấy xanh là push; lỗi trên OS khác để người dùng báo lại; ở đây khác ở Agent không có máy Windows hay macOS, nên dùng CI làm máy thử và đọc log từng dòng "not ok" để tìm nguyên nhân (đường dẫn symlink, chữ hoa ổ đĩa, tên ngắn RUNNER~1). Người đọc sẽ muốn biết cách không cần máy thật vẫn kiểm được nền tảng khác.
