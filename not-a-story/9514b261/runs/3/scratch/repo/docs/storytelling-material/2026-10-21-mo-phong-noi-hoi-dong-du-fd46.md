---
id: 2026-10-21-mo-phong-noi-hoi-dong-du-fd46
code: M-A48T
aliases: [M-A48T]
date: 2026-10-21
repo: repo
status: raw
signals: [khac, dao_quyet_dinh]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:9514b261#L1901", "claude:9514b261#L2612", "claude:9514b261#L2630", "claude:9514b261#L2805", "claude:9514b261#L2930"]
hook: "Mô phỏng nói đủ 11 ghế, bảng model lại sai vì thiếu một công cụ"
tension: tuong_ma_hoa_ra
sides: ["Mô phỏng báo hội đồng chạy tầng flagship", "Thiếu herdr nên sai: thật ra là tầng frontier"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Mô phỏng nói hội đồng đủ 11 ghế, nhưng bảng model đưa ra sai vì mô phỏng thiếu herdr

**Bối cảnh:** Agent dùng bộ mô phỏng gán ghế để chuẩn bị hội đồng kiến trúc, chạy trong môi trường không có herdr session.
**Chuyện gì xảy ra:** Mô phỏng gán openai qua codex-cli-bwrap, nhưng phiên thật có herdr nên gán khác. Khi chạy explain với herdrPresent true thì kết quả đúng: các capability critical chạy tầng frontier chứ không phải flagship như agent đã nói. Deepseek và glm cũng không nằm trong chuỗi dự phòng vì tierFallback chỉ liệt kê bốn family. Agent đính chính trước khi chủ quyết định.
**Bài học:** Mô phỏng phải chạy với đúng biến môi trường của production. Nếu không, kết quả 'đủ ghế' chỉ đúng trong môi trường giả.
**Artefact:** Bảng ghế trước và sau đính chính. Không cần ảnh.
**Góc người ngoài:** cách làm phổ biến là Người dùng thường tin bảng đầu tiên AI đưa ra, không yêu cầu xác nhận bằng chạy thật, và không quay lại sửa khi có dữ liệu mới; ở đây khác ở Agent đã công khai nói 'bảng model em đưa trước đó sai', giải thích nguyên nhân (thiếu herdr, trần tầng), và làm lại bảng. Người đọc sẽ hỏi làm sao để AI tự đính chính như vậy mà không bị bỏ sót.
