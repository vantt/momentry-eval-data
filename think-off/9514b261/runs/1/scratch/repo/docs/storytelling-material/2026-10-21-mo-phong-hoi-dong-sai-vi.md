---
id: 2026-10-21-mo-phong-hoi-dong-sai-vi
date: 2026-10-21
repo: repo
status: raw
signals: []
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:9514b261#L1901", "claude:9514b261#L1906", "claude:9514b261#L2612", "claude:9514b261#L2630"]
hook: "Bảng 11 ghế hội đồng em đưa ra sai vì mô phỏng thiếu herdr"
tension: giup_ma_hai
sides: ["mô phỏng để biết ghế nào chạy model nào", "thiếu herdr nên bảng ghế sai, kể cả kết luận về trần model"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Mô phỏng hội đồng sai vì không có herdr: bảng 11 ghế của em hoá ra không đáng tin

**Bối cảnh:** fgOS chạy LLM qua nhiều CLI, mỗi family có nhiều đường (invocation). Trước khi mở hội đồng kiến trúc 11 ghế, cần biết ghế nào gán được qua đường nào.
**Chuyện gì xảy ra:** Bộ mô phỏng gán vai chạy không có môi trường herdr nên gán openai qua codex-cli-bwrap, trong khi phiên thật có herdr thì đường khác. Em đã nói trần maxTier=flagship chặn hội đồng; lệnh explain cho thấy các capability critical lên tầng frontier, nên bảng model sai ở các ghế critical. Em đính chính: bảng ghế trước đó không còn đáng tin, chỉ explain trên phiên có herdrPresent=true mới đúng.
**Bài học:** Mô phỏng gán vai phải chạy trong đúng môi trường thật; khi lệnh explain có sẵn, tin nó hơn bảng tự suy.
**Artefact:** Hai bảng ghế cạnh nhau: bảng mô phỏng không herdr và bảng explain có herdr. Bỏ tên tài khoản, chỉ giữ tên family và invocation.
**Góc người ngoài:** cách làm phổ biến là Chạy thẳng cho xong rồi mới biết ghế nào lỗi, hoặc tự đoán theo tên model trong cấu hình; ở đây khác ở Người đọc sẽ muốn có cách xem trước kế hoạch chạy tốn tiền mà không tốn tiền. Phiên này cũng cho thấy mô phỏng có thể sai nếu thiếu một thành phần môi trường, nên luôn phải đối chiếu lại.
