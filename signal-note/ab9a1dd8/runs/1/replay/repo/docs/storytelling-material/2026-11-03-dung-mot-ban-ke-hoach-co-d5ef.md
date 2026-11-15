---
id: 2026-11-03-dung-mot-ban-ke-hoach-co-d5ef
code: M-R80F
aliases: [M-R80F]
date: 2026-11-03
repo: repo
status: raw
signals: []
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:ab9a1dd8#L2009", "claude:ab9a1dd8#L2888", "claude:ab9a1dd8#L2893"]
hook: "Báo '45/45' bằng cách đối chiếu checkbox, không phải cảm giác"
tension: tuong_ma_hoa_ra
sides: ["Dev tưởng mình xong vì cảm giác", "Checkbox máy kiểm cho thấy tiến độ thật"]
strength: 1
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Dùng một bản kế hoạch có kiểm tra máy (ak plan validate) làm đầu vào cho một vòng /ak-cook --auto, và agent tự đối chiếu checkbox để báo tiến độ 45/45

**Chuyện gì xảy ra:** Dùng một bản kế hoạch có kiểm tra máy (ak plan validate) làm đầu vào cho một vòng /ak-cook --auto, và agent tự đối chiếu checkbox để báo tiến độ 45/45
**Góc người ngoài:** cách làm phổ biến là Dev làm một mình thường viết việc cần làm vào ghi chú hoặc todo, tự nhớ tiến độ, và báo "xong rồi" dựa trên cảm giác; ở đây khác ở Plan có cấu trúc (phase, checkbox, trạng thái) được máy kiểm và đếm, nên việc "đã xong" có số liệu để chứng minh. Người đọc sẽ hỏi vì sao agent không báo xong sớm hơn, và vì sao có vòng lặp đẩy nó tiếp tục.
