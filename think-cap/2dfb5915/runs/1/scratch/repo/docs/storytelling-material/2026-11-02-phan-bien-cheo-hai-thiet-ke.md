---
id: 2026-11-02-phan-bien-cheo-hai-thiet-ke
date: 2026-11-02
repo: repo
status: raw
signals: [người duyệt, đảo quyết định]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L3051", "claude:2dfb5915#L3070", "claude:2dfb5915#L3110", "claude:2dfb5915#L3144", "claude:2dfb5915#L3170"]
hook: "Hai agent tự thiết kế rồi phản biện chéo, cùng ra đúng 13 tool"
tension: khac
sides: ["Hai agent làm độc lập", "Cả hai hội tụ về cùng 13 tool"]
strength: 1
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Phản biện chéo hai thiết kế MCP: 13 tool, không code mode

**Bối cảnh:** Gộp hai MCP (kg và ohs) thành một để agent không phải chọn giữa hai cửa.
**Chuyện gì xảy ra:** Hai agent làm độc lập rồi phản biện chéo, hội tụ về 13 tool. Ước lượng định nghĩa tool mỗi phiên giảm từ khoảng 6,0 nghìn xuống khoảng 4,4 nghìn token, tính theo độ dài chuỗi, chưa đo bằng tokenizer. Code mode bị loại vì Claude Desktop không có shell. User chốt read do pkm tự đọc file, không chuyển sang OHS, vì OHS không đọc được note khi đang index.
**Bài học:** Đề xuất thiết kế đáng tin hơn sau khi một agent khác cố bác nó; ước lượng token phải ghi rõ là chưa đo.
**Artefact:** Bảng phương án A-D với cột token và số lượt gọi, ghi rõ là ước lượng.
