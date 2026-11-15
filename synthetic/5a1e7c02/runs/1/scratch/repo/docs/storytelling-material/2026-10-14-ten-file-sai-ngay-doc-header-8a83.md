---
id: 2026-10-14-ten-file-sai-ngay-doc-header-8a83
code: M-Y18J
aliases: [M-Y18J]
date: 2026-10-14
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:5a1e7c02"
sessions: ["claude:5a1e7c02"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:5a1e7c02#L4", "claude:5a1e7c02#L5", "claude:5a1e7c02#L6", "claude:5a1e7c02#L7", "claude:5a1e7c02#L8", "claude:5a1e7c02#L10"]
hook: "Tên file ghi 24/09, dòng đầu bên trong ghi 25/09"
tension: tuong_ma_hoa_ra
sides: ["Tên file nói ngày 24/09, agent định đổi tên các file khác theo mẫu đó", "Dòng đầu trong file P06 ghi 25/09, nội dung mới là nguồn đáng tin"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "Một nghiên cứu churn cho khách hàng nha khoa: 14 phỏng vấn bệnh nhân, cần bản tổng hợp nháp và dàn ý cho buổi báo cáo điều hành thứ Năm."
spine_context_lines: ["claude:5a1e7c02#L1"]
spine_want: Có bản tổng hợp nháp và dàn ý cho buổi báo cáo điều hành.
spine_want_lines: ["claude:5a1e7c02#L1"]
spine_obstacle: Hai file phỏng vấn lệch mẫu tên.
spine_obstacle_lines: ["claude:5a1e7c02#L4"]
spine_action: Đổi tên hai file theo ngày ghi trong header; file P06 đổi thành 25/09 chứ không phải 24/09 như tên file.
spine_action_lines: ["claude:5a1e7c02#L5", "claude:5a1e7c02#L8"]
spine_outcome: Cả 14 file đều theo cùng một mẫu tên.
spine_outcome_lines: ["claude:5a1e7c02#L10"]
completeness: 5
---

# Tên file sai ngày: đọc header trước khi đổi tên

**Bối cảnh:** 14 file phỏng vấn được đặt tên theo ngày, trong đó hai file lệch mẫu tên.
**Chuyện gì xảy ra:** Agent thấy hai file lệch mẫu và đề xuất đổi tên theo mẫu 'Pxx_yyyy-mm-dd'. Người dùng yêu cầu kiểm tra ngày ghi trong nội dung trước, và dòng đầu của file P06 ghi 25/09 chứ không phải 24/09 như tên file. Agent đổi P03 và P06 theo ngày trong header, và người dùng xác nhận. Chuyện nhỏ này cho thấy tên file có thể sai trong khi metadata bên trong mới là nguồn đáng tin.
**Bài học:** Đừng coi tên file là nguồn sự thật về ngày. Đọc metadata trong file trước khi đổi tên, và ghi lại cả tên cũ để truy ngược.
**Artefact:** Ảnh terminal lệnh ls trước và sau khi đổi tên, kèm dòng header của file. Che tên thư mục khách hàng và mọi tên trong header.
