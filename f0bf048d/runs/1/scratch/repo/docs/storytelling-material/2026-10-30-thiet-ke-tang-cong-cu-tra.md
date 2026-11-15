---
id: 2026-10-30-thiet-ke-tang-cong-cu-tra
date: 2026-10-30
repo: repo
status: raw
signals: []
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:f0bf048d#L1414", "claude:f0bf048d#L1439", "claude:f0bf048d#L1654"]
hook: "Thêm tool trả phí chỉ một dòng, và agent tự cộng dồn tiền"
tension: it_ma_nhieu
sides: ["bật add-on trả phí chỉ bằng một dòng manifest", "agent tự đếm chi phí và hỏi chủ khi vượt $1 mỗi issue"]
strength: 1
stakes: 2
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Thiết kế tầng công cụ trả phí theo bậc: mặc định miễn phí, bật add-on trả phí (DataForSEO) bằng một dòng trong manifest từng khách; thiếu add-on thì plan không tạo MCP server đó. Kèm chỉ dẫn agent cộng dồn chi phí mỗi lần gọi và hỏi chủ khi vượt $1 mỗi issue.

**Chuyện gì xảy ra:** Thiết kế tầng công cụ trả phí theo bậc: mặc định miễn phí, bật add-on trả phí (DataForSEO) bằng một dòng trong manifest từng khách; thiếu add-on thì plan không tạo MCP server đó. Kèm chỉ dẫn agent cộng dồn chi phí mỗi lần gọi và hỏi chủ khi vượt $1 mỗi issue.
**Góc người ngoài:** cách làm phổ biến là Hoặc dùng tool miễn phí cho tất cả, hoặc gắn key trả phí chung cho mọi agent và hy vọng không tốn nhiều; ở đây khác ở Feature flag cho chi phí theo từng khách, kèm ước tính chi phí thật (khoảng $2–5/khách/tháng) trước khi quyết định. Người đọc muốn biết cách để agent có công cụ mạnh mà không đốt tiền ngoài ý muốn. Đồng thời nhận ra giới hạn $1 mới là chỉ dẫn chưa có chốt chặn cứng.
