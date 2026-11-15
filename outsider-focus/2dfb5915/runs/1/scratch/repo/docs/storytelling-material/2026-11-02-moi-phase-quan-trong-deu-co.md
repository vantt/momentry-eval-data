---
id: 2026-11-02-moi-phase-quan-trong-deu-co
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [hotspot, outsider]
lines: ["claude:2dfb5915#L591", "claude:2dfb5915#L607", "claude:2dfb5915#L614", "claude:2dfb5915#L1038", "claude:2dfb5915#L1045", "claude:2dfb5915#L1950"]
hook: "Test xanh hết, nhưng agent đọc code vẫn tìm ra lỗi mức High"
tension: tuong_ma_hoa_ra
sides: ["Test xanh nghĩa là code ổn", "Agent review chỉ đọc, không chạy, vẫn bắt được lỗi nặng"]
strength: 2
stakes: 2
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Mọi phase quan trọng đều có một agent review độc lập đọc code (không chạy), ra báo cáo mức High/Medium, rồi gửi lại cho đúng agent đã viết để sửa trên nhánh của nó, rồi mới merge.

**Chuyện gì xảy ra:** Mọi phase quan trọng đều có một agent review độc lập đọc code (không chạy), ra báo cáo mức High/Medium, rồi gửi lại cho đúng agent đã viết để sửa trên nhánh của nó, rồi mới merge.
**Góc người ngoài:** cách làm phổ biến là Tự review lại code do AI sinh, hoặc không review mà chỉ dựa vào test xanh. Review xong thì tự sửa tay; ở đây khác ở Reviewer chỉ ra những lỗi mà test không bắt được, như pipe stderr đầy làm treo cả tiến trình, build lỗi giữa chừng để lại index sai mãi, truy vấn chạy vô hạn. Vòng 'review, gửi lại người viết, sửa' tận dụng ngữ cảnh sẵn có của agent viết. Dev dùng AI hằng ngày sẽ muốn mẫu quy trình này.
