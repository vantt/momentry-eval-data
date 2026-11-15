---
id: 2026-11-02-hook-chan-lenh-vi-chua-chu-40f9
code: M-68FB
aliases: [M-68FB]
date: 2026-11-02
repo: repo
status: raw
signals: [rang_buoc_thiet_ke]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L75", "claude:c4caee3c#L612", "claude:c4caee3c#L791", "claude:c4caee3c#L3746"]
hook: "Hook chặn mọi lệnh có chữ 'build', agent không build nổi"
tension: giup_ma_hai
sides: ["Hook sinh ra để bảo vệ", "Chặn luôn npm run build, mỗi lần phải xin phép"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hook chặn lệnh vì chứa chữ build hoặc node_modules

**Bối cảnh:** Hook an toàn của môi trường chặn lệnh theo chuỗi ký tự, không theo ngữ cảnh. Cùng lúc agent cần chạy build và kiểm test.
**Chuyện gì xảy ra:** Hook chặn các lệnh có chứa node_modules hoặc build, nên agent không thể chạy npm run build và không thể kiểm thư mục đầu ra. Agent đặt đầu ra là build/ thay vì dist/ với lý do tương tự, rồi sửa file test bằng công cụ Edit thay vì lệnh shell. Mỗi lần bị chặn cần một bước xin phép riêng.
**Bài học:** Công cụ chặn theo chuỗi có thể chặn cả việc hợp lệ. Kiểm trước các từ khoá bị chặn khi chọn tên thư mục và tên script.
**Artefact:** Thông báo chặn của hook (không nhạy cảm).
