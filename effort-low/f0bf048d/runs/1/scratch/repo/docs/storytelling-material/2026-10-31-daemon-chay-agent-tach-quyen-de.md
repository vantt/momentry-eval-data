---
id: 2026-10-31-daemon-chay-agent-tach-quyen-de
date: 2026-10-31
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, nguyên nhân bất ngờ]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L1794", "claude:f0bf048d#L1843", "claude:f0bf048d#L1861", "claude:f0bf048d#L1891", "claude:f0bf048d#L2284", "claude:f0bf048d#L2394", "claude:f0bf048d#L2578"]
hook: "Một trang web chèn lệnh vào agent SEO là có thể thành chủ cả máy"
tension: nho_ma_to
sides: ["Agent SEO chỉ đọc một trang web có lệnh chèn", "Chuỗi giao việc dẫn tới user có docker, gần như root, và PAT của chủ"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Daemon chạy agent: tách quyền để agent không thành chủ hệ thống

**Bối cảnh:** Hệ thống Multica chạy nhiều agent AI trên một máy, trong đó daemon đăng nhập bằng PAT của chủ nên agent có thể mượn quyền chủ. Phiên này thiết kế lại quyền để agent không leo thang được.
**Chuyện gì xảy ra:** Một agent SEO bị chèn lệnh qua trang web có thể giao việc cho System Operator, mà System Operator chạy dưới user vantt có quyền docker (gần như root). Phản biện độc lập chỉ ra 3 lỗ khẩn cấp, gồm mã đăng nhập dev 6 ký tự trong .env. Giai đoạn 0 đã tắt daemon ops, tạo user agents-opc riêng và thay PAT cũ của chủ (thu hồi, PAT mới 90 ngày), nên agent không còn đường thành chủ.
**Bài học:** Chặn bằng cơ chế (quyền Unix, quyền Multica, token riêng), đừng dựa vào lời dặn trong prompt, vì nội dung web có thể ghi đè lời dặn.
**Artefact:** Bảng lộ trình giai đoạn 0–4 trong plans/2026-10-31-agent-permissions.md; che token, email, IP tailnet.
