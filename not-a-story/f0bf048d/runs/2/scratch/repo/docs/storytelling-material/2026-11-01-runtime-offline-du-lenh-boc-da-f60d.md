---
id: 2026-11-01-runtime-offline-du-lenh-boc-da-f60d
code: M-SDHG
aliases: [M-SDHG]
date: 2026-11-01
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, dao_quyet_dinh]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L2862", "claude:f0bf048d#L2870", "claude:f0bf048d#L2885", "claude:f0bf048d#L2908", "claude:f0bf048d#L2929", "claude:f0bf048d#L2937", "claude:f0bf048d#L2947"]
hook: "Đổi tên lệnh bọc xong, runtime tắt vì daemon không dò lại"
tension: giup_ma_hai
sides: ["Đổi tên lệnh theo tài khoản cho gọn", "Daemon chỉ dò lại khi profile đổi nên runtime offline"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Runtime offline dù lệnh bọc đã có: daemon chỉ dò lại khi profile đổi

**Bối cảnh:** Ba runtime (pi và omp) đã được khai báo. Runtime OpenAI của pi vẫn offline dù lệnh bọc đã có.
**Chuyện gì xảy ra:** Ban đầu agent đặt lệnh bọc theo tên pi-openai-codex. Người vận hành yêu cầu đổi tên theo tài khoản là pi-openai-tetnu. Đổi tên xong, daemon không tìm thấy lệnh và bỏ qua profile. Daemon chỉ kiểm lại profile khi profile bị sửa, nên agent tắt rồi bật lại profile và runtime lên ngay ở cả hai workspace.
**Bài học:** Daemon không tự dò lại profile khi lệnh bọc xuất hiện sau đó. Sau khi tạo lệnh, phải sửa profile để kích hoạt dò lại.
**Artefact:** Bảng ba runtime với lệnh bọc, model mặc định và trạng thái online.
