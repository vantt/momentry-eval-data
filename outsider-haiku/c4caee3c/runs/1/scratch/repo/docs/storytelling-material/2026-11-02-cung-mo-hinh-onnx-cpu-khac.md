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
hook: "Cùng mô hình, khác đời CPU, điểm eval lệch từ 0,735 ra 0,728"
tension: tuong_ma_hoa_ra
sides: ["tưởng cùng mô hình thì điểm cố định", "điểm đổi theo lớp CPU"]
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
**Góc người ngoài:** cách làm phổ biến là Phổ biến là hạ ngưỡng hoặc cập nhật số đo cho khớp CI khi cổng đỏ, vì đó là cách nhanh nhất; ở đây khác ở Agent chọn sửa nguồn của sai lệch và giữ nguyên ngưỡng; người đọc muốn biết làm sao nhận ra một lỗi thật sự là lỗi đo, không phải lỗi code.
