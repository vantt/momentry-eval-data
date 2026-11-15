---
id: 2026-11-02-danh-gia-tren-du-lieu-rieng-40f9
code: M-RZWX
aliases: [M-RZWX]
date: 2026-11-02
repo: repo
status: raw
signals: [rang_buoc_thiet_ke]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L2046", "claude:c4caee3c#L3633", "claude:c4caee3c#L3645", "claude:c4caee3c#L3797", "claude:c4caee3c#L3822", "claude:c4caee3c#L3824"]
hook: "Chấm trên dữ liệu riêng mà đầu ra không để lộ chữ nào"
tension: cam_ma_van_lot
sides: ["Cổng chỉ in số tổng hợp", "Chế độ chi tiết phải chặn ghi vào repo hay symlink"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đánh giá trên dữ liệu riêng: chỉ in số tổng hợp, không để lộ nội dung

**Bối cảnh:** Golden set và vault là dữ liệu riêng của chủ dự án. Quy tắc không cho đưa câu hỏi, tên note hay nội dung ra repo, CI hay log.
**Chuyện gì xảy ra:** Cổng đánh giá riêng được thiết kế để chỉ in số tổng hợp. Chế độ chi tiết ghi file theo từng câu ra ngoài repo, quyền 0600, và từ chối nếu đường dẫn nằm trong repo hoặc qua symlink. Một agent trên máy khác đẩy kết quả lên một nhánh riêng. Lead đọc báo cáo, sửa lỗi so sánh đường dẫn NFD, merge, rồi xoá nhánh. Test cho thấy đầu ra không chứa nội dung.
**Bài học:** Thiết kế đánh giá dữ liệu nhạy cảm từ đầu: chỉ số tổng hợp ra log, chi tiết đi ra ngoài repo, và có test kiểm chứng.
**Artefact:** Mẫu định dạng số tổng hợp (không chứa dữ liệu).
