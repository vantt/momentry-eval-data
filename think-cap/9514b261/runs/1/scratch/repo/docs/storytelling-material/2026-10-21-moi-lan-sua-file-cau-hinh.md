---
id: 2026-10-21-moi-lan-sua-file-cau-hinh
date: 2026-10-21
repo: repo
status: raw
signals: []
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:9514b261#L2213", "claude:9514b261#L2422", "claude:9514b261#L2438", "claude:9514b261#L3038", "claude:9514b261#L3847"]
hook: "Mọi lần sửa cấu hình đều sao lưu trước, chuỗi thay phải khớp đúng một lần"
tension: none
sides: []
strength: 0
stakes: 0
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Mọi lần sửa file cấu hình đều được sao lưu có dấu thời gian trước. Khi thay chuỗi trong file, agent dùng script có khẳng định rằng chuỗi cần thay chỉ xuất hiện đúng một lần. Kết quả probe cũ được chuyển vào thư mục riêng, không xoá.

**Chuyện gì xảy ra:** Mọi lần sửa file cấu hình đều được sao lưu có dấu thời gian trước. Khi thay chuỗi trong file, agent dùng script có khẳng định rằng chuỗi cần thay chỉ xuất hiện đúng một lần. Kết quả probe cũ được chuyển vào thư mục riêng, không xoá.
**Góc người ngoài:** cách làm phổ biến là Thường người ta sửa thẳng bằng sed hoặc chỉnh tay, và chỉ sao lưu khi đã lỡ làm hỏng; ở đây khác ở Khẳng định 'đúng một lần' ngăn việc thay nhầm hoặc thay thiếu khi file đã đổi. Giữ kết quả cũ thay vì xoá giúp đối chiếu sau này. Người đọc muốn biết vì sao làm kỹ như vậy khi sửa config.
