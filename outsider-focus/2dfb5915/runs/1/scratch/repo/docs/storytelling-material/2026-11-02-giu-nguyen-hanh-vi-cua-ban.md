---
id: 2026-11-02-giu-nguyen-hanh-vi-cua-ban
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:2dfb5915#L371", "claude:2dfb5915#L382", "claude:2dfb5915#L474", "claude:2dfb5915#L1445", "claude:2dfb5915#L1859", "claude:2dfb5915#L2144"]
hook: "Viết lại sang Rust mà không đổi một byte đầu ra: 712 lời gọi tool khớp hết"
tension: none
sides: []
strength: 1
stakes: 3
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Giữ nguyên hành vi của bản Python khi viết lại sang Rust bằng một bộ so khớp tự động: dựng 'golden' (dump toàn bộ bảng index, 81 câu đáp án, 712 lời gọi tool, CLI, handshake MCP) từ bản Python ở một commit được ghim, rồi mỗi lần push CI so bản Rust với golden. CI không cần Python hay token.

**Chuyện gì xảy ra:** Giữ nguyên hành vi của bản Python khi viết lại sang Rust bằng một bộ so khớp tự động: dựng 'golden' (dump toàn bộ bảng index, 81 câu đáp án, 712 lời gọi tool, CLI, handshake MCP) từ bản Python ở một commit được ghim, rồi mỗi lần push CI so bản Rust với golden. CI không cần Python hay token.
**Góc người ngoài:** cách làm phổ biến là Viết lại bằng cách đọc code cũ rồi viết unit test mới. Cùng lắm có vài test thủ công so đầu ra. Hiếm ai ghim commit tham chiếu và commit cả bộ đầu ra chuẩn vào repo; ở đây khác ở Người đọc sẽ hỏi 'làm sao biết bản mới đúng y bản cũ?'. Ở đây câu trả lời là một con số đo được (64/64 mục, 0 lệch) chạy trong CI trên cả ba hệ điều hành. Có cả cơ chế sửa một dòng golden thì phải báo đúng file:dòng để chứng minh bộ so không bị 'mù'. Chạy chế độ private chỉ in số lệch, không lộ dữ liệu vault thật.
