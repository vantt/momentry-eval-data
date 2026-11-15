---
id: 2026-10-29-nho-mot-lan-tra-cuu-nguon-c455
code: M-1BFV
aliases: [M-1BFV]
date: 2026-10-29
repo: repo
status: raw
signals: [dao_quyet_dinh, nguoi_duyet_may_soan]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:0faf0bb2#L1326", "claude:0faf0bb2#L2310", "claude:0faf0bb2#L2313"]
hook: "Đã đặt reviewPolicy human_only, agent vẫn tự đóng task sau 26 giây"
tension: tuong_ma_hoa_ra
sides: ["Tưởng reviewPolicy human_only chặn được agent tự đóng task", "Hoá ra chỉ executionPolicy mới là cổng review thật"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Nhờ một lần tra cứu nguồn, phát hiện spike Paperclip bị ghi nhầm: 'reviewPolicy' không chặn được việc agent tự đóng task

**Bối cảnh:** Trong spike Paperclip, một task được đặt reviewPolicy human_only nhưng agent vẫn tự chuyển sang done. Lúc đầu kết luận là Paperclip thiếu luồng duyệt.
**Chuyện gì xảy ra:** Task SEN-3 đặt reviewPolicy human_only, nhưng agent tự đóng task (done) sau 26 giây. Đọc lại doc/execution-semantics.md cho thấy reviewPolicy chỉ áp khi trả lời một xác nhận, còn executionPolicy mới là cổng review thật. Phải sửa lại kết luận trong tài liệu so sánh (§6.3, §8) và trong lesson.
**Bài học:** Một cờ ‘chỉ người duyệt’ chưa chắc là cổng cứng; đọc đúng cơ chế (xác nhận hay luồng duyệt) trước khi kết luận hệ thống thiếu tính năng.
**Artefact:** Bảng so sánh reviewPolicy và executionPolicy trong docs/comparison-aicoworker-vs-paperclip.md (che tên đường dẫn vault nếu có).
**Góc người ngoài:** cách làm phổ biến là Người làm một mình thường sửa lỗi im lặng hoặc để nguyên tài liệu cũ; ít khi công khai đính chính đến mức ghi thành một mục riêng; ở đây khác ở Người đọc muốn biết vì sao phiên này chủ động 'đính chính' thay vì che đi, và việc đó giữ tài liệu tin cậy ra sao.
