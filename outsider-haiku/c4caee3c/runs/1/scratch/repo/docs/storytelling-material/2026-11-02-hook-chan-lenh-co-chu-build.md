---
id: 2026-11-02-hook-chan-lenh-co-chu-build
date: 2026-11-02
repo: repo
status: raw
signals: [Ràng buộc định hình thiết kế, khác]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:c4caee3c#L75", "claude:c4caee3c#L612", "claude:c4caee3c#L791", "claude:c4caee3c#L3746"]
hook: "Hook chặn mọi lệnh có chữ 'build', cả git check-ignore"
tension: cam_ma_van_lot
sides: ["hook chặn lệnh chứa chữ build và node_modules", "vẫn sửa được file test bằng công cụ Edit"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hook chặn lệnh có chữ 'build' và 'node_modules': đổi cách làm việc

**Bối cảnh:** Một hook trong repo chặn các lệnh có chứa chữ build hoặc node_modules.
**Chuyện gì xảy ra:** Lệnh rm -rf node_modules bị chặn. Lệnh có chữ build, kể cả git check-ignore, bị chặn. Sửa file test buộc phải dùng công cụ Edit thay vì shell. Agent phải đổi tên thư mục đầu ra và đổi cách kiểm tra.
**Bài học:** Hook an toàn có thể làm chậm mọi bước; đọc thông báo chặn trước khi viết lại lệnh.
**Artefact:** Thông báo chặn đã rút gọn.
**Góc người ngoài:** cách làm phổ biến là Thông thường người ta hoặc đổi tên lệnh, hoặc hỏi user có muốn nới luật, vì một bộ lọc chặn từ khoá kiểu này thường là bẫy để tránh việc; ở đây khác ở Agent lách một rào chắn của harness theo cách hợp lệ nhưng không báo cho user là có rào đó; người đọc muốn biết ranh giới giữa 'lách hợp lệ' và 'lách trái phép' nằm ở đâu.
