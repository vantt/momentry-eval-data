---
id: 2026-11-02-co-force-bi-tach-thanh-hai-3c6e
code: M-BPEB
aliases: [M-BPEB]
date: 2026-11-02
repo: repo
status: raw
signals: [dao_quyet_dinh]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1797", "claude:2dfb5915#L2144"]
hook: "Một cờ --force tắt luôn bước bảo vệ cấu hình"
tension: nho_ma_to
sides: ["Cờ --force chỉ định cho phép cài vị trí lạ", "Nó tắt luôn cả kiểm Claude Desktop đang chạy"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Cờ --force bị tách thành hai cờ riêng

**Bối cảnh:** Cài khi pkm nằm ngoài thư mục chuẩn như Downloads cần một cờ ghi đè.
**Chuyện gì xảy ra:** Ban đầu --force vừa bỏ qua kiểm Claude Desktop đang chạy, vừa cho phép cài từ vị trí bất thường. Agent tách thành --allow-any-location để cờ này không tắt luôn bước bảo vệ cấu hình. Đây là thêm một cờ, không đổi tên lệnh nào.
**Bài học:** Một cờ mà gộp hai quyền khác nhau sẽ vô tình tắt cả hai bước bảo vệ. Tách ra khi thiết kế cờ.
