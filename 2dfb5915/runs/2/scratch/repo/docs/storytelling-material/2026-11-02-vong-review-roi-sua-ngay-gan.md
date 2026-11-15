---
id: 2026-11-02-vong-review-roi-sua-ngay-gan
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L591", "claude:2dfb5915#L819", "claude:2dfb5915#L1045", "claude:2dfb5915#L1781"]
hook: "Gần như mỗi lần merge, review đều tìm ra lỗi High"
tension: tuong_ma_hoa_ra
sides: ["code đã viết xong, CI xanh", "review vẫn tìm ra lỗi High mỗi lần"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Vòng review rồi sửa ngay: gần như mỗi merge đều có lỗi High

**Bối cảnh:** Sau mỗi module lớn, một agent review độc lập đọc code và chạy thử.
**Chuyện gì xảy ra:** Review OHS ra 2 High, review vault và schema ra 1 High cùng vài Medium, review index ra 2 High, review crate pkm ra 2 High. Mỗi lần, agent viết module được gọi quay lại sửa trên nhánh của nó, rồi merge sau khi CI xanh.
**Bài học:** Review độc lập sau mỗi merge tìm được lỗi mà test của người viết bỏ sót, nhất là lỗi treo và lỗi trên đường xấu.
**Artefact:** Bảng số lỗi theo mức và module.
**Góc người ngoài:** cách làm phổ biến là Dev dùng AI thường tự đọc diff của agent rồi sửa tay, hoặc chỉ chạy test rồi tin kết quả. Review bằng một agent khác rồi chuyển tiếp lại cho tác giả là rất hiếm; ở đây khác ở Cách này bắt được lỗi mà test không thấy: lỗi treo vì stderr, lỗi hết bộ nhớ vì alias bomb, build lỗi giữa chừng để lại dữ liệu cũ. Agent tác giả giữ nguyên ngữ cảnh nên sửa nhanh, và người dùng không phải đọc code.
