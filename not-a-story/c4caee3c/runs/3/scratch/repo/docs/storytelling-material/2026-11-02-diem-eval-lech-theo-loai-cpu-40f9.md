---
id: 2026-11-02-diem-eval-lech-theo-loai-cpu-40f9
code: M-A8R2
aliases: [M-A8R2]
date: 2026-11-02
repo: repo
status: raw
signals: [khac, nguyen_nhan_bat_ngo, dao_quyet_dinh]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:c4caee3c#L3312", "claude:c4caee3c#L3349", "claude:c4caee3c#L3370", "claude:c4caee3c#L3388", "claude:c4caee3c#L3415"]
hook: "Cùng một mục, hai loại CPU, hai điểm: 0,728 và 0,735"
tension: tuong_ma_hoa_ra
sides: ["Baseline 0,735 tưởng đúng ở mọi máy", "Runner đo ra 0,728, điểm lệch theo loại CPU"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Điểm eval lệch theo loại CPU, cổng chất lượng đỏ vì baseline ghi trên máy khác

**Bối cảnh:** Quantized ONNX cho số hơi khác nhau theo loại CPU của runner GitHub. Baseline ghi trên máy của lead không khớp với runner.
**Chuyện gì xảy ra:** Mục upstream-no-pack đo được 0,728 trên runner, baseline ghi là 0,735, chênh vượt tolerance 0,005. Lead không hạ baseline mà đổi cổng sang so với upstream được đo trong cùng lần chạy, còn baseline chỉ còn báo trôi. Khi đo chênh lệch của gói Mac Intel, ba runner EPYC cho số giống hệt nhau nhưng runner loại khác cho số lệch, nên cổng chỉ đếm kết quả trên EPYC.
**Bài học:** Đừng so số đo chất lượng giữa các loại máy. Đo baseline trong cùng lần chạy, trên cùng loại máy.
**Artefact:** Bảng số đo của ba runner, không kèm nội dung câu hỏi.
**Góc người ngoài:** cách làm phổ biến là Thường người ta chỉ đọc dòng lỗi cuối rồi sửa thử, hoặc re-run cho đến khi xanh; ở đây khác ở Agent đo lại trên nhiều máy, phát hiện kết quả phụ thuộc loại CPU và sửa cổng so sánh thay vì hạ ngưỡng. Người đọc sẽ muốn biết cách phân biệt 'lỗi cần sửa' với 'số đo thay đổi'.
