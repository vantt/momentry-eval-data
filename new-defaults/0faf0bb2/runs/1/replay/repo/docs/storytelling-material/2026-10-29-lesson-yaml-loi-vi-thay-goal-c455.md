---
id: 2026-10-29-lesson-yaml-loi-vi-thay-goal-c455
code: M-DWE3
aliases: [M-DWE3]
date: 2026-10-29
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:0faf0bb2#L590", "claude:0faf0bb2#L596", "claude:0faf0bb2#L599", "claude:0faf0bb2#L602", "claude:0faf0bb2#L603", "claude:0faf0bb2#L606", "claude:0faf0bb2#L613", "claude:0faf0bb2#L1903"]
hook: "Chuỗi 'domains:' khớp nhầm 'core_domains:' làm hỏng cả file lesson"
tension: nho_ma_to
sides: ["Thay phần goal bằng một đoạn python nhỏ", "'domains:' khớp nhầm 'core_domains:', hỏng cả file YAML"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Lesson YAML lỗi vì thay goal mới: chuỗi 'domains:' khớp nhầm vào 'core_domains:'

**Bối cảnh:** Pass distill ghi bài học vào file YAML. Khi đổi goal bằng script thay chuỗi, lỗi xuất hiện ở chỗ không ai nghĩ tới.
**Chuyện gì xảy ra:** Validator báo YAML lỗi thụt dòng ở dòng 38. Agent thay phần goal bằng python, nhưng chỉ mục 'domains:' khớp nhầm vào 'core_domains:' của goal cũ, làm hỏng cấu trúc file. Sửa bằng cách cắt lại đúng đoạn mới. Sau đó script ghi lesson còn văng lỗi Node do chuỗi escape trong heredoc, và một lệnh sed thay chuỗi cũng lỗi. Cuối cùng 30 lesson được ghi thành công.
**Bài học:** Thay đoạn văn bản trong file cấu hình bằng vị trí substring rất dễ khớp nhầm. Hãy neo theo dòng đầy đủ, hoặc parse YAML rồi ghi lại.
**Artefact:** Terminal báo 'bad indentation of a mapping entry (38:3)' và sau đó 'wrote 30 lessons'. Đường dẫn đã che.
