---
id: 2026-10-29-hai-du-an-doc-lap-cung
date: 2026-10-29
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L641", "claude:0faf0bb2#L1794", "claude:0faf0bb2#L1814"]
hook: "Một câu UPDATE đánh số task cho hai dự án, không cần khoá"
tension: it_ma_nhieu
sides: ["Chỉ một câu UPDATE ... RETURNING", "Cấp số nguyên tử, không khoá, không trùng"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hai dự án độc lập cùng đánh số task bằng một câu UPDATE RETURNING

**Bối cảnh:** Khi distill Paperclip và Kaneo, mình thấy cả hai cùng cách cấp mã task dạng PAP-123 hoặc KAN-12. Đây là bài học đầu tiên có bằng chứng từ hai nguồn.
**Chuyện gì xảy ra:** Cả hai dùng một câu UPDATE ... RETURNING trên bộ đếm của công ty hoặc project, nên việc cấp số là nguyên tử mà không cần khoá hay Durable Object. Điểm xếp hạng của bài học này tăng từ evidence 2 lên 3 sau khi có Kaneo. Phía client sinh id ngẫu nhiên dễ trùng khi nhiều người cùng ghi.
**Bài học:** Đánh số dễ đọc nên để server cấp bằng một câu UPDATE trên bộ đếm, không sinh ở client.
**Artefact:** Đoạn SQL dạng UPDATE ... RETURNING đã rút gọn.
