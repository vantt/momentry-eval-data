---
id: 2026-11-02-cung-mo-hinh-onnx-cpu-khac
date: 2026-11-02
repo: repo
status: raw
signals: [Nguyên nhân bất ngờ, Đảo quyết định có lý do]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:c4caee3c#L3349", "claude:c4caee3c#L3370", "claude:c4caee3c#L3903", "claude:c4caee3c#L3912"]
hook: "Cùng mô hình, khác CPU, điểm eval khác: 0,735 thành 0,728"
tension: tuong_ma_hoa_ra
sides: ["Tưởng cùng mô hình thì điểm cố định", "Đổi lớp CPU là điểm đổi theo"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Cùng mô hình ONNX, CPU khác, số eval khác: 0,735 thành 0,728

**Bối cảnh:** Cổng chất lượng so điểm eval tiếng Anh với baseline ghi trên máy khác. Máy local đo 0,735 còn runner CI đo 0,728.
**Chuyện gì xảy ra:** Agent ban đầu cho rằng điểm này cố định. Thực tế điểm thay đổi theo lớp CPU: một lớp cho một kết quả, lớp khác cho kết quả khác. Quyết định: cổng so với upstream đo trong cùng một lần chạy, baseline ghi chỉ dùng để báo trôi. Phép đo pin-effect chỉ tính kết quả chạy trên EPYC và thử lại tối đa 3 lần. Trên bản vantt.4, bản ghim cho vi-snippet tốt hơn 0,024, từ 0,951 lên 0,975.
**Bài học:** Số eval dùng lượng tử hoá không tái lập qua phần cứng; hãy so tương đối trong cùng một lần chạy.
**Artefact:** Bảng CPU và số đo theo hạng mục.
**Góc người ngoài:** cách làm phổ biến là Lưu file baseline số liệu vào repo rồi so với ngưỡng cố định; CI đỏ thì tăng tolerance hoặc cập nhật baseline; ở đây khác ở Ít người nghĩ số eval ML phụ thuộc loại CPU runner. Cách 'đo đối chứng cùng lượt chạy' loại hẳn flaky mà không nới dung sai. Người đọc có eval/benchmark trên CI sẽ muốn áp dụng.
