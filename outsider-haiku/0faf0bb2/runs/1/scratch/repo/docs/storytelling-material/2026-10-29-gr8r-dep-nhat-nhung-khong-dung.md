---
id: 2026-10-29-gr8r-dep-nhat-nhung-khong-dung
date: 2026-10-29
repo: repo
status: raw
signals: [ràng buộc thiết kế, artefact nhìn được]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L3302", "claude:0faf0bb2#L3329", "claude:0faf0bb2#L3332"]
hook: "Giao diện đẹp nhất lại tệ nhất: sửa comment xong, F5 máy khác là mất"
tension: tuong_ma_hoa_ra
sides: ["gr8r đẹp nhất trong ba ứng viên", "sửa comment chỉ nằm localStorage, máy khác F5 là mất"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# gr8r đẹp nhất nhưng không dùng được: cùng thao tác sửa comment, ba cách lưu khác nhau

**Bối cảnh:** Repo gr8r được nhiều người biết vì giao diện 'calm'. Khi đánh giá làm nền, mình so sánh thao tác sửa một comment giữa gr8r, Circle và Kaneo.
**Chuyện gì xảy ra:** gr8r sửa thẳng dữ liệu trong bộ nhớ rồi ghi cả khối JSON vào localStorage, người khác không thấy và F5 máy khác là mất. Circle sửa trong store zustand khởi tạo từ dữ liệu mẫu, tải lại là về mẫu. Kaneo gọi API, server lưu, WebSocket cập nhật các trình duyệt khác. gr8r không có license, chỉ có 3 commit và khoảng 80 chỗ ghi dữ liệu rải rác.
**Bài học:** Thiết kế đẹp không thay thế được license và lớp dữ liệu. Khi học từ một repo đẹp, đếm xem có bao nhiêu chỗ ghi dữ liệu trước khi quyết định.
**Artefact:** Bảng ba cột: gr8r, Circle, Kaneo, cùng hàng 'sửa comment làm gì'.
