---
id: 2026-10-29-agent-biet-dung-lai-hoi-chu-c455
code: M-F570
aliases: [M-F570]
date: 2026-10-29
repo: repo
status: raw
signals: [rang_buoc_thiet_ke, artefact_nhin_duoc]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L3691", "claude:0faf0bb2#L3709", "claude:0faf0bb2#L3712"]
hook: "Agent thà dừng hỏi giá 350.000đ còn hơn tự bịa số liệu"
tension: tuong_ma_hoa_ra
sides: ["Người ta tưởng AI sẽ tự điền số cho xong việc", "Mai dừng lại hỏi chủ giá và hạn đặt trước, bài trả lại hai lần mới đạt"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent biết dừng lại hỏi chủ thay vì tự bịa số liệu bán hàng

**Bối cảnh:** Trong workflow bài đăng Facebook, agent Mai được giao viết bài có giá và hạn chót ưu đãi, nhưng chủ chưa cung cấp các con số này.
**Chuyện gì xảy ra:** Long trả lại bài hai lần vì thiếu giá. Mai dừng lại và hỏi chủ giá (350.000đ) và hạn đặt trước (15/01), nói rõ không tự bịa số liệu bán hàng. Sau khi chủ comment, Mai điền vào và Long duyệt đạt, đưa issue sang in_review cho chủ.
**Bài học:** Ràng buộc 'không bịa số liệu' làm agent tạm dừng và hỏi người; vòng hỏi-đáp qua comment đủ để hoàn tất một bước workflow.
**Artefact:** Ảnh chụp chuỗi comment SEN-2 (che tên khách và email).
