---
id: 2026-10-29-go-cong-cu-xong-van-con-c455
code: M-485J
aliases: [M-485J]
date: 2026-10-29
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:0faf0bb2#L2431", "claude:0faf0bb2#L2440", "claude:0faf0bb2#L2452", "claude:0faf0bb2#L2469", "claude:0faf0bb2#L2547", "claude:0faf0bb2#L2556", "claude:0faf0bb2#L2572", "claude:0faf0bb2#L2590", "claude:0faf0bb2#L2613", "claude:0faf0bb2#L2615", "claude:0faf0bb2#L2624"]
hook: "Gỡ công cụ rồi, runtime vẫn giữ 6 file cache và 2 transcript"
tension: cam_ma_van_lot
sides: ["Đã gỡ sạch thư mục cài đặt", "Ba file chỉ mục runtime vẫn nhớ tên session của công cụ"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Gỡ công cụ xong vẫn còn dấu vết trong runtime

**Bối cảnh:** Đã gỡ CLI và xoá thư mục dữ liệu khoảng 2,4 GB của công cụ điều phối.
**Chuyện gì xảy ra:** Quét lại sau khi gỡ vẫn thấy 6 file cache và 2 transcript ở dạng '.deleted'. Ba file chỉ mục của runtime (sessions, system-prompt-reports, advisor-sessions) còn giữ tên các session của công cụ. Sau khi dọn thêm, grep toàn bộ thư mục runtime không còn chữ khoá tên công cụ. Công cụ tích hợp để dấu vết ở phía runtime, không chỉ trong thư mục cài đặt.
**Bài học:** Khi dọn một tích hợp, quét cả phía runtime đã nhận dữ liệu từ nó, không chỉ thư mục cài đặt. Kết thúc khi grep ra 0 kết quả.
**Artefact:** Kết quả grep 0 dòng. Che đường dẫn cá nhân.
**Góc người ngoài:** cách làm phổ biến là Người dùng thường tự cài thử một công cụ, chạy xong thì quên các tiến trình, cổng, thư mục và cache còn sót lại; dọn dẹp thường là xoá thư mục bằng tay và không kiểm tra lại; ở đây khác ở Trước mỗi lần cài, agent ghi lại thứ sẽ thay đổi (cổng, file, service); khi user bảo dọn thì quét lại toàn máy, xoá cả transcript và cache liên quan, rồi xác nhận bằng lệnh kiểm tra. Người đọc sẽ hỏi vì sao làm được vậy mà không sót gì.
