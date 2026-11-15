---
id: 2026-10-14-khao-sat-va-phong-van-xep-8a83
code: M-YVVN
aliases: [M-YVVN]
date: 2026-10-14
repo: repo
status: raw
signals: [so_truoc_so_sau, khac]
source: "chat Claude, claude:5a1e7c02"
sessions: ["claude:5a1e7c02"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:5a1e7c02#L23", "claude:5a1e7c02#L46", "claude:5a1e7c02#L47", "claude:5a1e7c02#L48", "claude:5a1e7c02#L49"]
hook: "Khảo sát 412 người được cho là 'củng cố' phỏng vấn, nhưng thứ hạng đảo ngược"
tension: tuong_ma_hoa_ra
sides: ["Agent viết khảo sát củng cố phỏng vấn về giá", "Khảo sát xếp 'quên nhắc nhở' đầu với 97, giá chỉ đứng sau; thứ hạng đảo ngược"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một người làm đang tổng hợp 14 phỏng vấn và khảo sát 412 bệnh nhân đã ngừng quay lại phòng khám nha khoa, để trình bày cho ban điều hành. Người làm tin rằng khảo sát củng cố phỏng vấn, nhưng thứ hạng thực tế đảo ngược: phỏng vấn nhắc đến giá nhiều nhất (7 người), còn khảo sát xếp 'quên hoặc không có nhắc nhở' đầu với 97, giá chỉ sau đó. Người dùng AI để viết báo cáo nghiên cứu nên biết rằng AI cũng có thể nói 'xác nhận' khi số liệu thực ra mâu thuẫn."
audience: dev dùng AI để viết báo cáo hoặc phân tích khảo sát
spine_context: "Một người làm đang tổng hợp 14 phỏng vấn và khảo sát 412 bệnh nhân đã ngừng quay lại phòng khám nha khoa, để chuẩn bị buổi trình bày cho ban điều hành thứ Năm."
spine_context_lines: ["claude:5a1e7c02#L1"]
spine_want: Muốn có bản tổng hợp sơ bộ và dàn ý cho buổi trình bày điều hành.
spine_want_lines: ["claude:5a1e7c02#L1"]
spine_obstacle: Phỏng vấn và khảo sát xếp lý do rời đi theo thứ hạng khác nhau.
spine_obstacle_lines: ["claude:5a1e7c02#L23", "claude:5a1e7c02#L49"]
spine_turn: "Tưởng khảo sát củng cố phỏng vấn; hoá ra thứ hạng đảo ngược: phỏng vấn nêu giá nhiều nhất, còn khảo sát xếp 'quên hoặc không có nhắc nhở' đầu với 97."
spine_turn_lines: ["claude:5a1e7c02#L23", "claude:5a1e7c02#L49"]
spine_action: Chạy truy vấn trên khảo sát rồi kết luận rằng kết quả củng cố phỏng vấn.
spine_action_lines: ["claude:5a1e7c02#L47", "claude:5a1e7c02#L48", "claude:5a1e7c02#L49"]
spine_outcome: Danh sách có chín phát hiện ứng viên; cả mục giá và mục nhắc nhở đều có mặt.
spine_outcome_lines: ["claude:5a1e7c02#L51"]
spine_takeaway: "Khi hai nguồn cho thứ hạng khác nhau, hãy trình bày cả hai và nêu lý do như cỡ mẫu hay cách hỏi, đừng gọi kết quả là củng cố."
spine_takeaway_lines: ["claude:5a1e7c02#L23", "claude:5a1e7c02#L49"]
completeness: 7
---

# Khảo sát và phỏng vấn xếp hạng lý do rời đi khác nhau

**Góc kể:** Một người làm đang tổng hợp 14 phỏng vấn và khảo sát 412 bệnh nhân đã ngừng quay lại phòng khám nha khoa, để trình bày cho ban điều hành. Người làm tin rằng khảo sát củng cố phỏng vấn, nhưng thứ hạng thực tế đảo ngược: phỏng vấn nhắc đến giá nhiều nhất (7 người), còn khảo sát xếp 'quên hoặc không có nhắc nhở' đầu với 97, giá chỉ sau đó. Người dùng AI để viết báo cáo nghiên cứu nên biết rằng AI cũng có thể nói 'xác nhận' khi số liệu thực ra mâu thuẫn.
**Bối cảnh:** Khảo sát 412 bệnh nhân đã lapse với câu hỏi chọn nhiều đáp án, đặt cạnh 14 phỏng vấn sâu.
**Chuyện gì xảy ra:** Trong 14 phỏng vấn, nhóm giá có 7 người còn nhắc nhở chỉ có 2. Khảo sát 412 người lại xếp 'quên hoặc không có nhắc nhở' đứng đầu với 97, rồi 'chi phí cao hơn mong đợi' 88 và 'tìm được chỗ rẻ hơn' 61. Agent viết rằng khảo sát 'củng cố' phỏng vấn, trong khi thứ hạng thực tế đảo ngược. Kết quả này là căn cứ để chọn nhắc nhở tự động làm một trong ba phát hiện.
**Bài học:** Khi hai nguồn cho thứ hạng khác nhau, hãy trình bày cả hai và nêu lý do (cỡ mẫu, cách hỏi), đừng gọi kết quả này là củng cố.
**Artefact:** Biểu đồ cột kép: tỉ lệ đề cập trong phỏng vấn và tỉ lệ chọn trong khảo sát, cùng một thang phần trăm, các lý do xếp theo cùng thứ tự.
