---
id: 2026-10-29-kaneo-noi-that-sua-comment-di-c455
code: M-BEB0
aliases: [M-BEB0]
date: 2026-10-29
repo: repo
status: raw
signals: [artefact_nhin_duoc, so_truoc_so_sau]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L3313", "claude:0faf0bb2#L3314", "claude:0faf0bb2#L3321", "claude:0faf0bb2#L3329", "claude:0faf0bb2#L3332"]
hook: "Giao diện gr8r sửa comment chỉ ghi localStorage, người khác không thấy"
tension: tuong_ma_hoa_ra
sides: ["Giao diện đẹp, trông như đã hoạt động", "Sửa comment chỉ nằm trong localStorage của máy mình"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Kaneo 'nối thật': sửa comment đi qua API chứ không ghi vào localStorage

**Bối cảnh:** Chủ hỏi 'Kaneo nối thật là sao?' sau khi so sánh với gr8r và Circle.
**Chuyện gì xảy ra:** Một comment đi qua hook, fetcher, Hono RPC client có kiểu lấy từ code server, rồi PUT, kiểm tra zod và ghi Postgres, và phát sự kiện qua WebSocket. Với gr8r, sửa comment chỉ ghi cả khối JSON vào localStorage nên người khác không thấy. Kaneo có khoảng 30 nhóm fetcher.
**Bài học:** Kiểu dữ liệu dùng chung giữa server và UI giúp đổi tên field bị bắt ngay lúc biên dịch.
**Artefact:** Sơ đồ luồng sửa comment ba cột: gr8r, Circle, Kaneo.
