---
id: 2026-11-05-scanner-bao-mat-bao-11-canh
date: 2026-11-05
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, ràng buộc định hình thiết kế]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:6a207191#L1304", "claude:6a207191#L1318", "claude:6a207191#L1324", "claude:6a207191#L2372", "claude:6a207191#L2375"]
hook: "7 cảnh báo critical, nhưng đều chỉ là chữ trong tài liệu"
tension: cam_ma_van_lot
sides: ["Scanner báo 7 critical, 1 high, 3 medium", "Tất cả chỉ là mô tả, không phải lệnh skill chạy, và quét lại vẫn đủ 11"]
strength: 2
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
**Góc người ngoài:** cách làm phổ biến là Gặp cảnh báo bảo mật thì hoặc bỏ qua hết ('chắc false positive'), hoặc sửa chữ cho scanner im đi mà không xem lại thật sự; ở đây khác ở Agent không chỉ nói 'false positive' mà còn đối chiếu từng cảnh báo với dòng cụ thể trong tài liệu và xác nhận hai script không tải hay chạy gì. Nó cũng nhận rằng người duyệt sẽ thấy đúng các cảnh báo này nên cần ghi chú trước. Người đọc muốn biết cách phân loại này.
