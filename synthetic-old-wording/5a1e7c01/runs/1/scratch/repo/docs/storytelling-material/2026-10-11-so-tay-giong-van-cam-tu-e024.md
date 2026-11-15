---
id: 2026-10-11-so-tay-giong-van-cam-tu-e024
code: M-ATX5
aliases: [M-ATX5]
date: 2026-10-11
repo: repo
status: raw
signals: [ràng buộc định hình cách làm]
source: "chat Claude, claude:5a1e7c01"
sessions: ["claude:5a1e7c01"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:5a1e7c01#L3", "claude:5a1e7c01#L6", "claude:5a1e7c01#L30", "claude:5a1e7c01#L31", "claude:5a1e7c01#L32", "claude:5a1e7c01#L33", "claude:5a1e7c01#L34", "claude:5a1e7c01#L35", "claude:5a1e7c01#L37"]
hook: "Grep bắt quả tang từ 'bí quyết' ngay trong tiêu đề phụ"
tension: cam_ma_van_lot
sides: ["Sổ tay giọng văn đã cấm từ 'bí quyết'", "Chính tiêu đề phụ vẫn dùng nó, chỉ grep mới thấy"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "Người làm viết bản tin email hằng tuần 'Thư Chủ Nhật', đang soạn số 48 về quỹ khẩn cấp."
spine_context_lines: ["claude:5a1e7c01#L1"]
spine_want: "Muốn tỉ lệ mở thư phục hồi, và bài số 48 đúng giọng văn sổ tay."
spine_want_lines: ["claude:5a1e7c01#L6", "claude:5a1e7c01#L7"]
spine_obstacle: Tỉ lệ mở thư 4 số gần đây tụt từ 52% xuống 31%.
spine_obstacle_lines: ["claude:5a1e7c01#L7"]
spine_action: "Đọc sổ tay và bản nháp, tìm từ cấm 'bí quyết' bằng grep, rồi đổi tiêu đề phụ."
spine_action_lines: ["claude:5a1e7c01#L31", "claude:5a1e7c01#L35"]
spine_outcome: Tiêu đề phụ đã đổi thành 'Giữ quỹ khỏi tay mình'; hai đoạn dài để người làm tự tách.
spine_outcome_lines: ["claude:5a1e7c01#L34", "claude:5a1e7c01#L37"]
completeness: 5
---

# Sổ tay giọng văn cấm từ 'bí quyết', và grep bắt đúng chỗ vi phạm

**Bối cảnh:** Sổ tay giọng văn của bản tin có quy tắc cấm một số từ, trong đó có từ 'bí quyết'. Chủ bản tin muốn agent kiểm tra bài theo quy tắc này.
**Chuyện gì xảy ra:** Agent tìm từ cấm bằng grep và thấy một tiêu đề phụ đang dùng nó. Agent đề xuất hai cách thay thế, chủ bản tin chọn 'Giữ quỹ khỏi tay mình'. Agent cũng chỉ ra hai đoạn dài 6 và 7 câu, và chủ bản tin tự quyết định cách tách.
**Bài học:** Biến quy tắc giọng văn thành từ khoá để máy tìm; soát bằng máy nhanh hơn đọc lại bằng mắt, và chỉ nên để người quyết câu chữ.
**Artefact:** Ảnh tiêu đề phụ trước và sau khi sửa, không cần trích cả đoạn bài.
