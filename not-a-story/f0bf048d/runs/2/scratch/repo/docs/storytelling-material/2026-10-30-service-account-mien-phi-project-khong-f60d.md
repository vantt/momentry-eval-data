---
id: 2026-10-30-service-account-mien-phi-project-khong-f60d
code: M-389E
aliases: [M-389E]
date: 2026-10-30
repo: repo
status: raw
signals: [rang_buoc_thiet_ke, so_truoc_so_sau]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L503", "claude:f0bf048d#L511", "claude:f0bf048d#L740", "claude:f0bf048d#L742"]
hook: "API miễn phí, project không billing, tiền thật nằm ở token Claude"
tension: tuong_ma_hoa_ra
sides: ["Tưởng tốn tiền ở API Google, nhưng chúng miễn phí", "Skill 15k ký tự nạp mỗi task mới là chỗ tốn tiền"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Service account miễn phí, project không billing, và chỗ tốn tiền thật là token Claude

**Bối cảnh:** Chủ hỏi việc dùng service account Google có tốn tiền không trước khi làm.
**Chuyện gì xảy ra:** Agent trả lời GA4 Data API và Search Console API đều miễn phí. Vượt hạn mức thì API trả lỗi 429, không tự tính tiền. Project tạo không gắn billing account nên không có đường tính tiền. Phần đáng kể là token Claude: skill dài khoảng 15k ký tự được nạp mỗi task, cộng dữ liệu MCP trả về. Các con số hạn mức là từ kiến thức của agent, chưa kiểm lại trên trang quota.
**Bài học:** Với API miễn phí, cách chắc nhất để không phát sinh phí là không gắn billing. Chi phí thật thường nằm ở token của agent chứ không ở API.
**Artefact:** Bảng chi phí từng API kèm hạn mức, đã ghi rõ con số nào chưa kiểm.
