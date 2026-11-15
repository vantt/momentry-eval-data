---
id: 2026-10-14-ten-file-sai-ngay-doc-header-8a83
code: M-Y18J
aliases: [M-Y18J]
date: 2026-10-14
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:5a1e7c02"
sessions: ["claude:5a1e7c02"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:5a1e7c02#L4", "claude:5a1e7c02#L5", "claude:5a1e7c02#L6", "claude:5a1e7c02#L7", "claude:5a1e7c02#L8", "claude:5a1e7c02#L10"]
hook: "Tên file ghi 24/09, dòng đầu bên trong lại ghi 25/09"
tension: tuong_ma_hoa_ra
sides: ["Tên file tưởng là nguồn đúng, agent định đổi tên theo đó", "Ngày trong header file P06 mới đúng, lệch một ngày"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một nghiên cứu về việc khách rời đi (churn) ở một khách hàng nha khoa, đang tổng hợp 14 buổi phỏng vấn bệnh nhân cho buổi trình bày lãnh đạo thứ Năm. Agent đề xuất đổi tên hai file lệch mẫu theo ngày trong tên, nhưng người làm nghĩ mình ghi âm một buổi vào ngày 25 chứ không phải 24. Mở dòng đầu file ra thì đúng là 25/09, nên tên file đã sai. Ai làm phỏng vấn định tính nên đọc metadata trong file trước khi tin tên file."
audience: "người làm phỏng vấn và phân tích định tính, hay đặt tên file theo ngày"
spine_context: "Nghiên cứu churn (khách rời đi) cho một khách hàng nha khoa: 14 buổi phỏng vấn bệnh nhân, cần bản tổng hợp cho buổi trình bày lãnh đạo thứ Năm."
spine_context_lines: ["claude:5a1e7c02#L1"]
spine_want: "Có bản tổng hợp và dàn ý cho buổi trình bày, sau khi dọn tên file phỏng vấn cho gọn."
spine_want_lines: ["claude:5a1e7c02#L1", "claude:5a1e7c02#L4"]
spine_obstacle: "Hai file lệch mẫu tên, và tên file có vẻ ghi sai ngày."
spine_obstacle_lines: ["claude:5a1e7c02#L4", "claude:5a1e7c02#L5"]
spine_turn: "Tưởng tên file ghi đúng ngày ghi âm; hoá ra dòng đầu bên trong file ghi 25/09, lệch một ngày so với tên."
spine_turn_lines: ["claude:5a1e7c02#L4", "claude:5a1e7c02#L7"]
spine_action: "Mở dòng đầu của P06 trước khi đổi tên, rồi đổi tên P03 và P06 theo ngày trong file."
spine_action_lines: ["claude:5a1e7c02#L5", "claude:5a1e7c02#L6", "claude:5a1e7c02#L8"]
spine_outcome: P06 thành P06_2026-09-25; agent báo cả 14 file theo cùng một mẫu (theo lời agent).
spine_outcome_lines: ["claude:5a1e7c02#L10"]
spine_takeaway: Đừng coi tên file là nguồn sự thật về ngày; đọc metadata trong file trước khi đổi tên.
spine_takeaway_lines: ["claude:5a1e7c02#L5", "claude:5a1e7c02#L7"]
completeness: 7
---

# Tên file sai ngày: đọc header trước khi đổi tên

**Góc kể:** Một nghiên cứu về việc khách rời đi (churn) ở một khách hàng nha khoa, đang tổng hợp 14 buổi phỏng vấn bệnh nhân cho buổi trình bày lãnh đạo thứ Năm. Agent đề xuất đổi tên hai file lệch mẫu theo ngày trong tên, nhưng người làm nghĩ mình ghi âm một buổi vào ngày 25 chứ không phải 24. Mở dòng đầu file ra thì đúng là 25/09, nên tên file đã sai. Ai làm phỏng vấn định tính nên đọc metadata trong file trước khi tin tên file.
**Bối cảnh:** 14 file phỏng vấn được đặt tên theo ngày, trong đó hai file lệch mẫu tên.
**Chuyện gì xảy ra:** Agent thấy hai file lệch mẫu và đề xuất đổi tên theo mẫu 'Pxx_yyyy-mm-dd'. Người dùng yêu cầu kiểm tra ngày ghi trong nội dung trước, và dòng đầu của file P06 ghi 25/09 chứ không phải 24/09 như tên file. Agent đổi P03 và P06 theo ngày trong header, và người dùng xác nhận. Chuyện nhỏ này cho thấy tên file có thể sai trong khi metadata bên trong mới là nguồn đáng tin.
**Bài học:** Đừng coi tên file là nguồn sự thật về ngày. Đọc metadata trong file trước khi đổi tên, và ghi lại cả tên cũ để truy ngược.
**Artefact:** Ảnh terminal lệnh ls trước và sau khi đổi tên, kèm dòng header của file. Che tên thư mục khách hàng và mọi tên trong header.
