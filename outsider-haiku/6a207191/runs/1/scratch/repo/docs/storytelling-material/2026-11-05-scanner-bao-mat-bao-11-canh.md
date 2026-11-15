---
id: 2026-11-05-scanner-bao-mat-bao-11-canh
date: 2026-11-05
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, ràng buộc định hình thiết kế]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:6a207191#L1304", "claude:6a207191#L1318", "claude:6a207191#L1324", "claude:6a207191#L2372", "claude:6a207191#L2375"]
hook: "Scanner báo 7 lỗi critical, nhưng cả 7 chỉ là chữ trong tài liệu"
tension: tuong_ma_hoa_ra
sides: ["11 cảnh báo, 7 mức critical", "đều là mô tả, không có lệnh nào được chạy"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Scanner bảo mật báo 11 cảnh báo, 7 critical đều là chữ trong tài liệu installer

**Bối cảnh:** Hub quét skill trước khi nhận bản gửi. Skill này là tài liệu về installer nên chứa đúng những mẫu như 'curl ... | sh' trong ví dụ.
**Chuyện gì xảy ra:** Quét 26 rule ra 11 cảnh báo: 7 critical rce.pipe-to-shell, 1 high persist.autostart, 3 medium privesc.command. Agent đọc từng vị trí và thấy đều là mô tả quy tắc, chú thích hoặc usage của mẫu, không phải lệnh skill tự chạy. Hai script kiểm tra chỉ đọc. Sau khi chỉnh, quét lại vẫn ra 11 cảnh báo, và người duyệt trên hub sẽ thấy đúng số đó.
**Bài học:** Scanner bắt theo mẫu chữ, mà tài liệu về một mối nguy luôn chứa đúng mẫu chữ đó. Hãy ghi rõ trong ghi chú gửi kèm để người duyệt phân loại nhanh.
**Artefact:** Bảng 11 cảnh báo gồm rule, vị trí và đánh giá. Không chụp đường dẫn máy.
