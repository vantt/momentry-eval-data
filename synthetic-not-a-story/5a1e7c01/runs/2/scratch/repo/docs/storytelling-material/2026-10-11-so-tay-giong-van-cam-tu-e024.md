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
hook: "grep bắt được chữ 'bí quyết' ngay trong tiêu đề phụ của chính sổ cấm nó"
tension: tuong_ma_hoa_ra
sides: ["sổ tay giọng văn cấm từ 'bí quyết'", "chính tiêu đề phụ của bản tin lại đang dùng từ đó"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "Bản tin 'Thư Chủ Nhật', người làm đang viết số 48 về quỹ khẩn cấp."
spine_context_lines: ["claude:5a1e7c01#L1"]
spine_want: Soát bài số 48 theo sổ tay giọng văn.
spine_want_lines: ["claude:5a1e7c01#L1"]
spine_obstacle: "Một tiêu đề phụ dùng từ 'bí quyết', mà sổ tay cấm từ này."
spine_obstacle_lines: ["claude:5a1e7c01#L32", "claude:5a1e7c01#L33"]
spine_action: Đổi tiêu đề phụ thành 'Giữ quỹ khỏi tay mình'.
spine_action_lines: ["claude:5a1e7c01#L34", "claude:5a1e7c01#L35"]
spine_outcome: Đã sửa tiêu đề phụ; hai đoạn dài được để người làm tự tách.
spine_outcome_lines: ["claude:5a1e7c01#L34", "claude:5a1e7c01#L37"]
completeness: 5
---

# Sổ tay giọng văn cấm từ 'bí quyết', và grep bắt đúng chỗ vi phạm

**Bối cảnh:** Sổ tay giọng văn của bản tin có quy tắc cấm một số từ, trong đó có từ 'bí quyết'. Chủ bản tin muốn agent kiểm tra bài theo quy tắc này.
**Chuyện gì xảy ra:** Agent tìm từ cấm bằng grep và thấy một tiêu đề phụ đang dùng nó. Agent đề xuất hai cách thay thế, chủ bản tin chọn 'Giữ quỹ khỏi tay mình'. Agent cũng chỉ ra hai đoạn dài 6 và 7 câu, và chủ bản tin tự quyết định cách tách.
**Bài học:** Biến quy tắc giọng văn thành từ khoá để máy tìm; soát bằng máy nhanh hơn đọc lại bằng mắt, và chỉ nên để người quyết câu chữ.
**Artefact:** Ảnh tiêu đề phụ trước và sau khi sửa, không cần trích cả đoạn bài.
