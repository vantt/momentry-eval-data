---
id: 2026-11-05-quet-bao-mat-chan-skill-vi
date: 2026-11-05
repo: repo
status: raw
signals: [người duyệt, nguyên nhân bất ngờ]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:6a207191#L1304", "claude:6a207191#L1318", "claude:6a207191#L2375", "claude:6a207191#L2404"]
hook: "Quét bảo mật báo 7 lỗi nghiêm trọng, toàn là chữ trong tài liệu"
tension: tuong_ma_hoa_ra
sides: ["11 phát hiện, 7 mức critical chặn skill", "Script chỉ đọc file, các mục chỉ là chữ trong tài liệu"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Quét bảo mật chặn skill vì 7 dòng 'curl | sh' nằm trong tài liệu hướng dẫn

**Bối cảnh:** Skill dạy cách viết installer nên có đoạn 'curl ... | sh' trong tài liệu và mẫu. Trước khi gửi, skillstation chạy quét bảo mật.
**Chuyện gì xảy ra:** Lần quét đầu báo 11 phát hiện: 7 critical rce.pipe-to-shell, 1 high persist.autostart, 3 medium privesc. Agent đọc lại hai script kiểm tra và kết luận chúng chỉ đọc file, không có hành vi nguy hiểm thật; các mục đều là chữ trong tài liệu. Người dùng chọn gửi kèm cảnh báo. Lần gửi sau quét ra đúng 11 phát hiện.
**Bài học:** Skill hướng dẫn cài đặt luôn trúng quy tắc pipe-to-shell. Hãy ghi chú cho người duyệt từ đầu thay vì để họ tự tìm lại.
**Artefact:** Bảng rule, mức độ và số lượng. Không kèm đường dẫn chi tiết.
**Góc người ngoài:** cách làm phổ biến là Người dùng thường hoặc bỏ qua cảnh báo bảo mật, hoặc sửa tài liệu cho máy quét im lặng mà không biết nguyên nhân; ở đây khác ở Agent phân biệt cảnh báo thật với cảnh báo do công cụ đọc nhầm, và để người dùng quyết định. Người đọc sẽ muốn cách xử lý cảnh báo có cơ sở thay vì bỏ qua hay né cho qua.
