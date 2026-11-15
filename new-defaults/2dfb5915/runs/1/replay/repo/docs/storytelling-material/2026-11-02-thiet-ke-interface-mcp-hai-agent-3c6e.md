---
id: 2026-11-02-thiet-ke-interface-mcp-hai-agent-3c6e
code: M-H32V
aliases: [M-H32V]
date: 2026-11-02
repo: repo
status: raw
signals: [dao_quyet_dinh, nguoi_duyet_may_soan]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L2965", "claude:2dfb5915#L2991", "claude:2dfb5915#L3029", "claude:2dfb5915#L3088", "claude:2dfb5915#L3100", "claude:2dfb5915#L3144", "claude:2dfb5915#L3170"]
hook: "Hai agent thiết kế riêng, ra 13 tool gần y hệt nhau"
tension: khac
sides: ["Hai agent làm độc lập, không nhìn nhau", "Kết quả gần trùng khớp, 13 tool"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Thiết kế interface MCP: hai agent độc lập, phản biện chéo, và từ chối code mode

**Bối cảnh:** Sau rc.1 cần gộp hai MCP (kg và ohs) thành một. Thiết kế cần chốt trước khi cố định tool signature.
**Chuyện gì xảy ra:** Hai agent (một brainstormer, một agent thiết kế độc lập dùng model mạnh nhất) đưa ra bộ 13 tool gần như trùng nhau, không dùng code mode. Sau phản biện chéo, người duyệt chọn đọc file trực tiếp thay vì chuyển sang OHS (vì OHS mất vài phút để index). Token định nghĩa tool giảm từ khoảng 6 nghìn xuống 3,8–4,4 nghìn (ước lượng theo ký tự, chưa đo bằng tokenizer).
**Bài học:** Với bộ tool nhỏ dùng trong Claude Desktop (không có shell), code mode kiểu meta-tool thêm lượt gọi mà không lợi; giữ tool rời và đo bằng dùng thật.
**Artefact:** Bảng so sánh phương án (token định nghĩa, số lượt gọi, công sức); không chứa câu hỏi thật.
**Góc người ngoài:** cách làm phổ biến là Người làm tự đặt tên tool và tham số theo cảm tính, rồi chỉnh khi gặp lỗi; ở đây khác ở Thiết kế được đo bằng số lượt gọi và số token định nghĩa cho các câu hỏi mẫu, và các điểm bất đồng được ghi lại cùng bằng chứng. Người đọc muốn biết cách đo token định nghĩa tool và cách so hai phương án.
