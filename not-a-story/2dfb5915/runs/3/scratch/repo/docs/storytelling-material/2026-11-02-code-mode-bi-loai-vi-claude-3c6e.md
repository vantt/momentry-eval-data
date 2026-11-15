---
id: 2026-11-02-code-mode-bi-loai-vi-claude-3c6e
code: M-XMXW
aliases: [M-XMXW]
date: 2026-11-02
repo: repo
status: raw
signals: [khac, dao_quyet_dinh]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L3009", "claude:2dfb5915#L3060", "claude:2dfb5915#L3070"]
hook: "Code mode bị loại vì Claude Desktop không có shell"
tension: chon_mot_mat_mot
sides: ["Code mode có thể giảm số tool cần gọi", "Claude Desktop không có shell, meta-tool còn làm tốn thêm lượt gọi"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Code mode bị loại vì Claude Desktop không có shell

**Bối cảnh:** Người dùng gợi ý cơ chế code mode của một repo khác để tham khảo.
**Chuyện gì xảy ra:** Cơ chế đó chạy mã trên shell của agent, còn Claude Desktop không có shell hay sandbox. Với khoảng 13 tool, meta-tool làm mỗi phiên tốn thêm lượt gọi và che mất bước chọn giữa find và search. Quyết định là không làm code mode ở phase 17, và ghi một điều kiện xem lại nếu có từ 2 câu trở lên vượt giới hạn lượt gọi.
**Bài học:** Kỹ thuật tốt ở môi trường này có thể hỏng ở môi trường khác. Kiểm tra các giả định về công cụ trước khi áp dụng.
