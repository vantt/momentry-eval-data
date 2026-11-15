---
id: 2026-11-01-runtime-offline-vi-doi-ten-lenh-f60d
code: M-1WC6
aliases: [M-1WC6]
date: 2026-11-01
repo: repo
status: raw
signals: [nguyên nhân gốc nhỏ, số trước/sau]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L2880", "claude:f0bf048d#L2885", "claude:f0bf048d#L2908", "claude:f0bf048d#L2932", "claude:f0bf048d#L2938", "claude:f0bf048d#L2948"]
hook: "Cài lệnh xong runtime vẫn offline, phải tắt rồi bật profile"
tension: tuong_ma_hoa_ra
sides: ["Cài lệnh còn thiếu là chạy", "Daemon chỉ dò lại khi profile đổi"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Runtime offline vì đổi tên lệnh bọc sau khi tạo profile: daemon chỉ dò lại khi profile đổi

**Bối cảnh:** Đã tạo sáu runtime profile cho ba tài khoản Codex, Grok và Gemini ở hai workspace.
**Chuyện gì xảy ra:** Tên lệnh bọc đổi từ theo nhà cung cấp sang theo tài khoản, và profile được tạo trước khi lệnh tồn tại. Daemon bỏ qua profile có lệnh chưa có. Sau khi cài lệnh, runtime vẫn offline; bật rồi tắt profile để daemon dò lại, và cả ba lên online ở cả hai workspace (từ 2 trên 3 lên 3 trên 3). Cách xử lý được ghi vào skill của System Operator.
**Bài học:** Sau khi tạo lệnh bọc, sửa profile một lần để kích hoạt dò lại; đặt tên lệnh theo tài khoản để nhiều tài khoản cùng nhà cung cấp không đụng nhau.
**Artefact:** Danh sách runtime với trạng thái online/offline (che id).
