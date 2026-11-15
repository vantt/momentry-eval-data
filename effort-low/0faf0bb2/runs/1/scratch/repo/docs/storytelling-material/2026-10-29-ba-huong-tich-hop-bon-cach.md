---
id: 2026-10-29-ba-huong-tich-hop-bon-cach
date: 2026-10-29
repo: repo
status: raw
signals: [artefact nhìn được, đảo quyết định có lý do]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L3872", "claude:0faf0bb2#L3927"]
hook: "Ba hệ thống, bốn cách đóng gói, không hệ nào gói nổi cả một công ty"
tension: tuong_ma_hoa_ra
sides: ["nền tảng nào cũng nói đóng gói được agent và công ty", "không hệ nào gói trọn công ty nhiều agent kèm workflow"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Ba hướng tích hợp, bốn cách đóng gói: vì sao không có hệ nào đóng gói được cả công ty OPC

**Bối cảnh:** Sau spike, cần chọn cách đóng gói agent và workflow để deploy một công ty OPC lặp lại được.
**Chuyện gì xảy ra:** Paperclip đóng gói được cả công ty theo chuẩn Agent Companies v1 nhưng thiếu workflow nhiều bước. AICoworker đóng gói một agent qua .agent nhưng không gói nhiều agent. Multica chỉ export được skill. Đề xuất gói OPC theo chuẩn mở cộng phần mở rộng WORKFLOW.md và công cụ deploy đa nền tảng.
**Bài học:** Khi chưa hệ nào làm đủ, chọn chuẩn mở làm lõi và viết phần thiếu thành phần mở rộng, thay vì chọn một nền tảng đang có.
**Artefact:** Bảng 3 hệ thống với cột 'đóng gói được' và 'thiếu'. Không che gì.
