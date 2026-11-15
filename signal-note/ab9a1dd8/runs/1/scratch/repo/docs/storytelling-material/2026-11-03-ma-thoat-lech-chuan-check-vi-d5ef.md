---
id: 2026-11-03-ma-thoat-lech-chuan-check-vi-d5ef
code: M-9VDD
aliases: [M-9VDD]
date: 2026-11-03
repo: repo
status: raw
signals: [dao_quyet_dinh, so_truoc_so_sau]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L256", "claude:ab9a1dd8#L264", "claude:ab9a1dd8#L889", "claude:ab9a1dd8#L908", "claude:ab9a1dd8#L1253", "claude:ab9a1dd8#L2230"]
hook: "Đổi mã thoát từ 2 sang 1: script cũ hiểu sai mà không báo"
tension: chon_mot_mat_mot
sides: ["Theo chuẩn: mã 1 là vi phạm", "Hook và script cũ hiểu mã 2 sẽ hiểu sai âm thầm"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Momentry là công cụ đọc transcript phiên làm việc với coding agent để nhặt chuyện đáng kể, và người làm muốn ai đó, người hay agent, chỉ đọc --help là tự cài và chạy được lần đầu. Ban đầu họ tin điều đó đã đủ, nhưng README thiếu bước lấy code và chưa có installer hay doctor, nên người mới không đi nổi từ con số 0. Khi thử bằng một agent mới, lệnh sửa lỗi được ghi thành câu văn nên agent kẹt ở lần đầu; sửa thành lệnh chạy được thì qua ngay. Ai viết hướng dẫn cho agent nên thử bằng agent mới trước khi tin nó."
audience: dev viết CLI và hướng dẫn cho agent
spine_context: Momentry là công cụ đọc transcript của phiên làm việc với coding agent để nhặt chuyện đáng kể; người làm đang chuẩn bị phân phối cho người dùng mới.
spine_context_lines: [profile]
spine_want: Người mới hoặc một agent chỉ đọc --help phải tự đi từ con số 0 tới lần chạy đầu thành công.
spine_want_lines: ["claude:ab9a1dd8#L236"]
spine_obstacle: "README thiếu bước lấy code, chưa có installer, phiên bản, doctor; init không tạo hộp chuyện nên quick start dừng giữa chừng."
spine_obstacle_lines: ["claude:ab9a1dd8#L236"]
spine_turn: "Tưởng --help và --json là đủ để agent tự cài và sửa lỗi; hoá ra lệnh sửa cho nguồn chặn chỉ là câu văn, agent kẹt ở lần thử đầu."
spine_turn_lines: ["claude:ab9a1dd8#L236", "claude:ab9a1dd8#L2230"]
spine_action: "Thêm installer, doctor, init, lệnh config privacy-add, và thử lại bằng một agent mới chỉ đọc --help."
spine_action_lines: ["claude:ab9a1dd8#L2230"]
spine_outcome: 232 test qua trên Linux; agent mới tự cài và đưa doctor tới ok ngay lần thử sau khi có lệnh chạy được.
spine_outcome_lines: ["claude:ab9a1dd8#L2230"]
spine_takeaway: "Hướng dẫn cho agent phải là lệnh chạy được, không phải câu văn; thử bằng một agent mới để bắt chỗ kẹt trước khi tin."
spine_takeaway_lines: ["claude:ab9a1dd8#L2230"]
completeness: 7
---

# Mã thoát lệch chuẩn: check vi phạm riêng tư thoát 2, đổi thành 1 là đổi hợp đồng công khai

**Góc kể:** Momentry là công cụ đọc transcript phiên làm việc với coding agent để nhặt chuyện đáng kể, và người làm muốn ai đó, người hay agent, chỉ đọc --help là tự cài và chạy được lần đầu. Ban đầu họ tin điều đó đã đủ, nhưng README thiếu bước lấy code và chưa có installer hay doctor, nên người mới không đi nổi từ con số 0. Khi thử bằng một agent mới, lệnh sửa lỗi được ghi thành câu văn nên agent kẹt ở lần đầu; sửa thành lệnh chạy được thì qua ngay. Ai viết hướng dẫn cho agent nên thử bằng agent mới trước khi tin nó.
**Bối cảnh:** CLI momentry công bố bảng mã thoát trong README và PRD. Skill yêu cầu 0 là xong, 1 là có lỗi, 2 là sai cú pháp.
**Chuyện gì xảy ra:** Đổi chuẩn làm nghĩa của 1 và 2 đảo ngược. Agent cảnh báo rằng pre-commit hook hoặc script đang hiểu thoát 2 là vi phạm riêng tư sẽ hiểu sai mà không báo lỗi. User chọn theo chuẩn. Assert trong test đổi từ 2 sang 1 ở ba file test, và CHANGELOG có mục Breaking.
**Bài học:** Đổi mã thoát là đổi API. Đổi cùng lúc với CHANGELOG và ghi rõ mục Breaking.
**Artefact:** Bảng mã thoát trước và sau khi đổi.
