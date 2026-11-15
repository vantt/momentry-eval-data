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
hook: "Mô phỏng thiếu một biến môi trường, bảng ghế sai hết"
tension: nho_ma_to
sides: ["Thiếu một biến herdr khi chạy mô phỏng", "openai gán sai đường, trần tầng bị tính sai"]
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
**Góc người ngoài:** cách làm phổ biến là Cấu hình xong thì chạy luôn, rồi xem lỗi khi nó xảy ra; ở đây khác ở Người đọc thấy việc kiểm tra không tốn chi phí và được làm trước, và cũng thấy rằng mô phỏng có thể sai (nó đã cho kết quả sai khi thiếu herdr), nên phải đối chiếu lại bằng lệnh giải thích trên phiên thật.
