---
id: 2026-11-02-hai-agent-thiet-ke-mcp-doc-3c6e
code: M-SCGG
aliases: [M-SCGG]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L3051", "claude:2dfb5915#L3070", "claude:2dfb5915#L3088", "claude:2dfb5915#L3098", "claude:2dfb5915#L3110"]
hook: "Hai agent làm riêng ra cùng kết luận, nhưng tính sai token"
tension: nguoi_dung_may_sai
sides: ["Hai agent đồng ý, con số 1,9 nghìn token có vẻ đúng", "Phản biện chéo cho thấy file thật tốn 3,3 đến 3,8 nghìn"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hai agent thiết kế MCP độc lập, phản biện chéo và sửa con số token

**Bối cảnh:** Cần chốt bộ tool MCP một cửa, gồm search, read và related.
**Chuyện gì xảy ra:** Hai agent làm độc lập và đi tới kết luận gần như trùng: giữ tool rời, không làm code mode, read do pkm tự đọc. Số token định nghĩa giảm từ khoảng 6,0 nghìn xuống 4,4 nghìn. Khi phản biện chéo, một agent chỉ ra bản kia tính thấp số token danh sách tool: 7 KB là khoảng 1,9 nghìn token, nhưng file thật 13.381 ký tự cho ra khoảng 3,3 đến 3,8 nghìn.
**Bài học:** Ước lượng token theo số ký tự dễ lệch. Hai thiết kế độc lập rồi phản biện chéo bắt được lỗi mà một agent đơn lẻ bỏ sót.
**Artefact:** Bảng so sánh các phương án (chụp báo cáo, không lộ đường dẫn).
**Góc người ngoài:** cách làm phổ biến là Một người viết spec rồi tự quyết, hoặc hỏi nhiều câu nhỏ rời rạc; ở đây khác ở Hai thiết kế gần như trùng nhau; phản biện chéo sửa được số token ước lượng và bắt lỗi compact() mà cả hai không nêu lúc đầu. Người đọc muốn biết cách tổ chức để ra quyết định nhanh mà không phải đoán.
