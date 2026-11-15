---
id: 2026-10-11-so-tay-giong-van-cam-tu-e024
code: M-ATX5
aliases: [M-ATX5]
date: 2026-10-11
repo: repo
status: raw
signals: [rang_buoc_thiet_ke]
source: "chat Claude, claude:5a1e7c01"
sessions: ["claude:5a1e7c01"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:5a1e7c01#L3", "claude:5a1e7c01#L6", "claude:5a1e7c01#L30", "claude:5a1e7c01#L31", "claude:5a1e7c01#L32", "claude:5a1e7c01#L33", "claude:5a1e7c01#L34", "claude:5a1e7c01#L35", "claude:5a1e7c01#L37"]
hook: "Lệnh grep bắt được chữ 'bí quyết' nằm ngay tiêu đề phụ"
tension: none
sides: []
strength: 0
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Sổ tay giọng văn cấm từ 'bí quyết', và grep bắt đúng chỗ vi phạm

**Bối cảnh:** Sổ tay giọng văn của bản tin có quy tắc cấm một số từ, trong đó có từ 'bí quyết'. Chủ bản tin muốn agent kiểm tra bài theo quy tắc này.
**Chuyện gì xảy ra:** Agent tìm từ cấm bằng grep và thấy một tiêu đề phụ đang dùng nó. Agent đề xuất hai cách thay thế, chủ bản tin chọn 'Giữ quỹ khỏi tay mình'. Agent cũng chỉ ra hai đoạn dài 6 và 7 câu, và chủ bản tin tự quyết định cách tách.
**Bài học:** Biến quy tắc giọng văn thành từ khoá để máy tìm; soát bằng máy nhanh hơn đọc lại bằng mắt, và chỉ nên để người quyết câu chữ.
**Artefact:** Ảnh tiêu đề phụ trước và sau khi sửa, không cần trích cả đoạn bài.
