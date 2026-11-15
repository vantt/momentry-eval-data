---
id: 2026-10-30-chi-phi-api-google-mien-phi-f60d
code: M-6YS7
aliases: [M-6YS7]
date: 2026-10-30
repo: repo
status: raw
signals: [so_truoc_so_sau]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L503", "claude:f0bf048d#L511"]
hook: "API Google miễn phí, nhưng 15k ký tự skill mỗi task mới tốn tiền"
tension: tuong_ma_hoa_ra
sides: ["Tưởng tốn tiền ở API Google", "Tiền thật đi vào token Claude nạp skill mỗi task"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chi phí: API Google miễn phí, chỗ tốn tiền là token Claude của agent

**Bối cảnh:** Chủ hỏi service account có bị tốn tiền không.
**Chuyện gì xảy ra:** Service account và key JSON miễn phí. GA4 và Search Console API không tính tiền nếu project không gắn billing, vượt hạn mức chỉ trả 429. Chi phí thật là token Claude: skill dài khoảng 15k ký tự được nạp vào mỗi task, cộng dữ liệu MCP trả về. Con số hạn mức là hiểu biết của agent, chưa kiểm lại trên trang quota hiện tại.
**Bài học:** Tách chi phí của API bên thứ ba khỏi chi phí LLM. Chi phí LLM tăng theo số lần agent được kích hoạt.
**Artefact:** Bảng chi phí theo thành phần, ghi rõ chỗ chưa kiểm.
