---
id: 2026-10-30-agent-kiem-chung-thong-tin-ben
date: 2026-10-30
repo: repo
status: raw
signals: []
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:f0bf048d#L1376", "claude:f0bf048d#L1377", "claude:f0bf048d#L1378", "claude:f0bf048d#L1388", "claude:f0bf048d#L2344", "claude:f0bf048d#L2351", "claude:f0bf048d#L2354", "claude:f0bf048d#L2367"]
hook: "Hỏi giá dịch vụ, agent tra tài liệu gốc thay vì trả lời theo trí nhớ"
tension: none
sides: []
strength: 0
stakes: 2
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent kiểm chứng thông tin bên ngoài trước khi trả lời, và nhận lỗi công khai khi sai. Khi được hỏi về giá, điều khoản hay quyền của một dịch vụ, nó tra tài liệu gốc thay vì trả lời theo trí nhớ. Khi phát hiện đề xuất trước đó sai (quyền đọc của repo riêng trên GitHub), nó nói rõ 'tôi đã nói sai' và đưa lựa chọn thay thế.

**Chuyện gì xảy ra:** Agent kiểm chứng thông tin bên ngoài trước khi trả lời, và nhận lỗi công khai khi sai. Khi được hỏi về giá, điều khoản hay quyền của một dịch vụ, nó tra tài liệu gốc thay vì trả lời theo trí nhớ. Khi phát hiện đề xuất trước đó sai (quyền đọc của repo riêng trên GitHub), nó nói rõ 'tôi đã nói sai' và đưa lựa chọn thay thế.
**Góc người ngoài:** cách làm phổ biến là AI thường trả lời từ dữ liệu huấn luyện, nêu giá hay giới hạn như thể chắc chắn, và khi sai thì ít khi quay lại sửa; ở đây khác ở Mỗi con số hay khẳng định đều có nguồn kiểm được, và các điểm chưa kiểm được gắn nhãn rõ. Người đọc muốn biết cách làm để agent không đưa ra thông tin sai với vẻ chắc chắn.
