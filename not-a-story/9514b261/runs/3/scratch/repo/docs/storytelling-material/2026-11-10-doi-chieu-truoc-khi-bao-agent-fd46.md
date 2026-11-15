---
id: 2026-11-10-doi-chieu-truoc-khi-bao-agent-fd46
code: M-0VPV
aliases: [M-0VPV]
date: 2026-11-10
repo: repo
status: raw
signals: []
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [outsider]
lines: []
hook: "AI báo cáo xong, agent đếm lại từng dòng rồi mới tin"
tension: tuong_ma_hoa_ra
sides: ["Báo cáo của sub-agent trông đầy đủ nên ai cũng tin luôn", "Agent chạy lại lệnh kiểm từng khẳng định rồi mới báo"]
strength: 2
stakes: 2
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đối chiếu trước khi báo: agent kiểm lại từng khẳng định quan trọng của sub-agent (đếm dòng, đọc lại file, chạy lại lệnh) rồi mới báo cho user, thay vì chuyển nguyên kết quả.

**Chuyện gì xảy ra:** Đối chiếu trước khi báo: agent kiểm lại từng khẳng định quan trọng của sub-agent (đếm dòng, đọc lại file, chạy lại lệnh) rồi mới báo cho user, thay vì chuyển nguyên kết quả.
**Góc người ngoài:** cách làm phổ biến là Phần lớn người dùng AI nhận báo cáo của agent/sub-agent rồi tin luôn, hoặc chỉ đọc lướt; ở đây khác ở Sub-agent đã nói sai nhiều lần trong phiên (số ADR, số mục 'provisional', giả định về chủ sở hữu). Agent kiểm lại và đính chính công khai, nên user biết chỗ nào đã kiểm và chỗ nào chỉ là lời agent khác. Người đọc sẽ hỏi: 'làm sao biết cái nào đáng tin?'.
