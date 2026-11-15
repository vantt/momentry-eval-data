---
id: 2026-11-02-release-rc-job-macos-bi-huy-3c6e
code: M-G4Z7
aliases: [M-G4Z7]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L3461", "claude:2dfb5915#L3551", "claude:2dfb5915#L3585", "claude:2dfb5915#L3624", "claude:2dfb5915#L3658"]
hook: "Job macOS chờ runner 15 phút rồi bị huỷ, không phải lỗi code"
tension: tuong_ma_hoa_ra
sides: ["Build đỏ, tưởng code hỏng", "Do chờ runner quá 15 phút; rerun còn gặp HTTP 500"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Release rc: job macOS bị huỷ vì chờ runner 15 phút, rerun gặp HTTP 500

**Bối cảnh:** Release workflow dựng binary cho bốn nền, gồm macOS.
**Chuyện gì xảy ra:** Job dựng binary macOS chờ runner quá 15 phút rồi bị GitHub huỷ, không phải lỗi code. Khi rerun job lỗi, API trả HTTP 500 lần đầu, lần hai mới nhận. Watch thoát sớm trước khi rerun xong, phải dùng vòng kiểm tra trạng thái. Cuối cùng release thành công với 7 file.
**Bài học:** Job phụ thuộc runner hiếm có thể bị huỷ vì chờ, phân biệt với lỗi code bằng log. Đừng tin lệnh watch khi job đang được chạy lại.
**Góc người ngoài:** cách làm phổ biến là Xem đỏ là lỗi code, sửa code, push lại; hoặc chờ mãi không biết nguyên nhân; ở đây khác ở Agent đọc log để phân loại 'job không khởi động, không phải lỗi code', rerun đúng job, và báo người dùng cách mở khoá thanh toán. Người đọc muốn biết cách đọc CI đỏ mà không sửa nhầm code.
