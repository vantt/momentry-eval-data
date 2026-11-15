---
id: 2026-10-29-lay-token-gateway-tu-proc-cua
date: 2026-10-29
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:0faf0bb2#L823", "claude:0faf0bb2#L827", "claude:0faf0bb2#L891", "claude:0faf0bb2#L894", "claude:0faf0bb2#L1119"]
hook: "Lấy token từ tiến trình đang chạy: không in ra, không lưu file, commit thoải mái"
tension: none
sides: []
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Lấy token gateway từ /proc của tiến trình đang chạy, không in ra màn hình

**Bối cảnh:** Script tạo agent và test cần token của gateway, nhưng script này được lưu trong repo để tái dùng.
**Chuyện gì xảy ra:** Lần chạy đầu lỗi KeyError vì biến môi trường chưa được export. Sau đó script đọc token từ environ của tiến trình đang lắng nghe cổng gateway, đưa thẳng vào cấu hình adapter. Token không hiện trên dòng lệnh và không nằm trong file, nên script có thể commit mà không lộ bí mật.
**Bài học:** Đọc bí mật từ tiến trình đang chạy thay vì file cấu hình để script chia sẻ được; đánh đổi là chỉ dùng được khi dịch vụ đang chạy.
**Artefact:** Không có.
