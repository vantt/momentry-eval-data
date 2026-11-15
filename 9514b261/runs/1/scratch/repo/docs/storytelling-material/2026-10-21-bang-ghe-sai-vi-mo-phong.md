---
id: 2026-10-21-bang-ghe-sai-vi-mo-phong
date: 2026-10-21
repo: repo
status: raw
signals: [đảo quyết định, người duyệt]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:9514b261#L1901", "claude:9514b261#L1913", "claude:9514b261#L1923", "claude:9514b261#L2612", "claude:9514b261#L2630"]
hook: "Bảng ghế đúng trên giấy, sai vì mô phỏng thiếu một biến"
tension: nho_ma_to
sides: ["mô phỏng chạy thiếu một biến môi trường", "bảng gán ghế lệch so với phiên thật"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Bảng ghế sai vì mô phỏng chạy không có herdr

**Bối cảnh:** Trước khi mở hội đồng, agent đã đưa cho người duyệt bảng 11 ghế lấy từ bộ mô phỏng gán vai.
**Chuyện gì xảy ra:** Bộ mô phỏng chạy không có biến herdr nên openai được gán qua một đường khác với phiên thật. Lệnh explain (có herdrPresent true) cho thấy capability mức critical nâng trần lên tầng frontier, khác giả định maxTier=flagship của agent. Agent đính chính ba điều trước khi người duyệt đồng ý, rồi dựng lại bảng từ explain.
**Bài học:** Mô phỏng phải chạy đúng môi trường thật. Những gì người duyệt đã thấy thì phải kiểm lại bằng lệnh của hệ thống trước khi chốt.
**Artefact:** Hai bảng ghế cũ và mới đặt cạnh nhau (family, tầng, đường dùng).
**Góc người ngoài:** cách làm phổ biến là Dev thường gọi thẳng nhiều model/API rồi mới biết cái nào lỗi hoặc hết quota; hiếm ai có bước 'dự diễn' việc phân công và dự phòng; ở đây khác ở Người đọc sẽ hỏi làm sao biết trước ai làm ghế nào mà không gọi model. Nhưng chính phiên này cũng cho thấy mô phỏng thiếu bối cảnh (không có herdr) cho bảng sai, và 'explain' mới là bản đúng, nên dry-run phải chạy trong đúng môi trường thật.
