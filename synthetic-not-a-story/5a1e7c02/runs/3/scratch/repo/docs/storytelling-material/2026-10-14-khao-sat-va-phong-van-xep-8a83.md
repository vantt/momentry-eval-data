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
hook: "Khảo sát 412 người 'củng cố' phỏng vấn, nhưng thứ hạng lại đảo ngược"
tension: tuong_ma_hoa_ra
sides: ["Agent nói khảo sát củng cố phỏng vấn, giá đứng đầu", "Khảo sát xếp quên nhắc nhở đầu với 97, giá chỉ xếp sau"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Khảo sát và phỏng vấn xếp hạng lý do rời đi khác nhau

**Bối cảnh:** Khảo sát 412 bệnh nhân đã lapse với câu hỏi chọn nhiều đáp án, đặt cạnh 14 phỏng vấn sâu.
**Chuyện gì xảy ra:** Trong 14 phỏng vấn, nhóm giá có 7 người còn nhắc nhở chỉ có 2. Khảo sát 412 người lại xếp 'quên hoặc không có nhắc nhở' đứng đầu với 97, rồi 'chi phí cao hơn mong đợi' 88 và 'tìm được chỗ rẻ hơn' 61. Agent viết rằng khảo sát 'củng cố' phỏng vấn, trong khi thứ hạng thực tế đảo ngược. Kết quả này là căn cứ để chọn nhắc nhở tự động làm một trong ba phát hiện.
**Bài học:** Khi hai nguồn cho thứ hạng khác nhau, hãy trình bày cả hai và nêu lý do (cỡ mẫu, cách hỏi), đừng gọi kết quả này là củng cố.
**Artefact:** Biểu đồ cột kép: tỉ lệ đề cập trong phỏng vấn và tỉ lệ chọn trong khảo sát, cùng một thang phần trăm, các lý do xếp theo cùng thứ tự.
