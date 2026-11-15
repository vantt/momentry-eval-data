---
id: 2026-10-21-chuoi-thay-the-quyet-dinh-36-fd46
code: M-2E8X
aliases: [M-2E8X]
date: 2026-10-21
repo: repo
status: raw
signals: [khac, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L1116", "claude:9514b261#L1121", "claude:9514b261#L1163", "claude:9514b261#L1212", "claude:9514b261#L1237"]
hook: "36 quyết định, 18 quan hệ thay thế, 4 cái chỉ nằm trong câu chữ"
tension: tuong_ma_hoa_ra
sides: ["Có sẵn dữ liệu quan hệ thay thế để biết quyết định nào còn hiệu lực", "5 trên 7 cặp chỉ thay một phần, 4 cái ghi trong câu chữ, có cái trỏ tới mã băm"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Forgent là nền tảng để xây app agent, và đội đang làm một bộ đọc để agent chỉ thấy quyết định còn hiệu lực, không đọc phải quyết định đã bị thay. Người làm tin rằng dữ liệu 'quyết định nào thay quyết định nào' đã đủ để dựng bộ đọc đó. Khi đếm trong nhật ký sự kiện thì chỉ 7 cặp quyết định nền tảng có khai quan hệ, 5 trên 7 chỉ thay một phần, và ít nhất 4 lần thay thế chỉ nằm trong câu chữ. Ai đang dựa vào chuỗi thay thế để lọc quyết định cũ nên kiểm trước khi tin máy đã đủ thông tin."
audience: dev làm app agent và dev lưu quyết định kiến trúc
spine_context: Forgent (fgOS) là tầng nền tảng để xây và chạy app agent. Đội đang làm bộ đọc để agent chỉ thấy quyết định còn hiệu lực.
spine_context_lines: [profile]
spine_want: "Bộ đọc tính ra tập quyết định hiệu lực, ẩn kết luận đã bị thay để agent không đọc nhầm."
spine_want_lines: ["claude:9514b261#L1128"]
spine_obstacle: "Quan hệ thay thế chưa đủ và chưa có cấu trúc: chỉ 7 cặp quyết định nền tảng có khai quan hệ, phần còn lại nằm trong câu chữ."
spine_obstacle_lines: ["claude:9514b261#L1237"]
spine_turn: "Tưởng chuỗi thay thế đã đủ để bộ đọc dựa vào; hoá ra chỉ 7 cặp có khai quan hệ, 5 trên 7 chỉ thay một phần."
spine_turn_lines: ["claude:9514b261#L1128", "claude:9514b261#L1237"]
spine_action: "Đếm 36 quyết định ADR và 18 quan hệ thay thế trong nhật ký, rồi đối chiếu id với state và index."
spine_action_lines: ["claude:9514b261#L1121", "claude:9514b261#L1212"]
spine_outcome: "Chưa đủ dữ liệu để tính tập hiệu lực: ít nhất 4 quyết định thay điều khoản chỉ ghi trong câu chữ, và một đích thay thế là mã băm tài liệu."
spine_outcome_lines: ["claude:9514b261#L1237"]
spine_takeaway: Quan hệ thay thế phải là dữ liệu có cấu trúc thì máy mới biết cái nào còn hiệu lực.
spine_takeaway_lines: ["claude:9514b261#L1237"]
completeness: 7
---

# Chuỗi thay thế quyết định: 36 ADR, 18 quan hệ, và ít nhất 4 quyết định chỉ nói trong câu chữ

**Góc kể:** Forgent là nền tảng để xây app agent, và đội đang làm một bộ đọc để agent chỉ thấy quyết định còn hiệu lực, không đọc phải quyết định đã bị thay. Người làm tin rằng dữ liệu 'quyết định nào thay quyết định nào' đã đủ để dựng bộ đọc đó. Khi đếm trong nhật ký sự kiện thì chỉ 7 cặp quyết định nền tảng có khai quan hệ, 5 trên 7 chỉ thay một phần, và ít nhất 4 lần thay thế chỉ nằm trong câu chữ. Ai đang dựa vào chuỗi thay thế để lọc quyết định cũ nên kiểm trước khi tin máy đã đủ thông tin.
**Bối cảnh:** Chủ hỏi reducer 'tập quyết định hiệu lực' có đủ dữ liệu chưa. Agent đếm trực tiếp trong event log.
**Chuyện gì xảy ra:** Trong 4679 sự kiện decision, 37 có scope. Trong 36 ADR có 8 quyết định mang quan hệ supersedes, tổng cộng 18 quan hệ. Với 7 cặp quyết định nền tảng, id khớp được nhưng 5 trên 7 chỉ thay một phần. Ít nhất 4 quyết định thay điều khoản chỉ được ghi trong câu chữ, và có đích thay thế không phải quyết định mà là một mã băm tài liệu. Dữ liệu vì vậy chưa đủ để tính tập hiệu lực.
**Bài học:** Muốn máy tính được cái nào còn hiệu lực, quan hệ thay thế phải là dữ liệu có cấu trúc, không được để trong văn bản.
**Artefact:** Bảng phân loại 7 cặp quan hệ, chỉ có số liệu. Không cần ảnh.
