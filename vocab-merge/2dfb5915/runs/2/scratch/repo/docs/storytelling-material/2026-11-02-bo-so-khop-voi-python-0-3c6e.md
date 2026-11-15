---
id: 2026-11-02-bo-so-khop-voi-python-0-3c6e
code: M-GZHD
aliases: [M-GZHD]
date: 2026-11-02
repo: repo
status: raw
signals: ["số trước, số sau", nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L474", "claude:2dfb5915#L860", "claude:2dfb5915#L1445", "claude:2dfb5915#L1859", "claude:2dfb5915#L3242"]
hook: "Python và Rust đều đúng, vậy mà CI Windows vẫn đỏ"
tension: tuong_ma_hoa_ra
sides: ["Hai bên so khớp đều chạy đúng", "Script so khớp mới là thứ sai, thiếu một dạng đường dẫn"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Bộ so khớp với Python: 0 lệch là kết quả của nhiều lần sửa đặc tả, không phải một lần chạy

**Bối cảnh:** Mục tiêu là Rust cho ra đúng từng byte so với bản Python trên vault thử kg-solo. Bộ so khớp (parity harness) đếm số mục khớp trên tổng 64 mục.
**Chuyện gì xảy ra:** Số mục 'chưa có' giảm từ 47 xuống 34, 15, 1, rồi 0 khi đủ 64/64. Lỗi trên CI Windows lộ ra vì đường dẫn Windows bị escape trong JSON không được che; Python và Rust đều đúng nhưng script so khớp thiếu một dạng đường dẫn. Thứ tự liệt kê file của hệ điều hành làm lệch điểm 'related' ở mức 1e-5, vượt ngưỡng 1e-6 của đặc tả, nên phải ghim thứ tự theo đường dẫn đã sắp.
**Bài học:** Khi so khớp hai bản triển khai, thứ tự liệt kê file của hệ điều hành có thể là nguồn lệch ẩn; ghim thứ tự rồi mới so sánh chặt.
**Artefact:** Bảng 'số mục khớp / chưa có / lệch' qua các lần chạy; không che gì thêm.
**Góc người ngoài:** cách làm phổ biến là Viết test đơn vị theo kỳ vọng tự nghĩ ra, hoặc so sánh thủ công vài ví dụ; ở đây khác ở Port sang ngôn ngữ khác mà dựa vào golden file sinh từ bản gốc, mọi lệch được gắn tên và có chủ đích. Người đọc muốn biết cách làm golden đủ tin cậy và cách xử lý lệch có chủ ý.
