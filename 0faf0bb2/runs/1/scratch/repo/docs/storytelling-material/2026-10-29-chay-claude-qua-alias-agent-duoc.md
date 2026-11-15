---
id: 2026-10-29-chay-claude-qua-alias-agent-duoc
date: 2026-10-29
repo: repo
status: raw
signals: [ràng buộc thiết kế, nguyên nhân bất ngờ]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L3406", "claude:0faf0bb2#L3409", "claude:0faf0bb2#L3412", "claude:0faf0bb2#L3747"]
hook: "Gõ 'claude' thường, thật ra agent chạy bỏ qua mọi quyền"
tension: tuong_ma_hoa_ra
sides: ["tưởng đang chạy Claude thông thường", "alias thêm --dangerously-skip-permissions, không sandbox"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chạy Claude qua alias: agent được bỏ qua mọi quyền, không có sandbox

**Bối cảnh:** Trước spike Multica + Claude, mình kiểm chế độ quyền của Claude trên máy. Lệnh claude thực chất là alias có sẵn cờ bỏ qua quyền.
**Chuyện gì xảy ra:** Kiểm tra cho thấy claude là alias của lệnh với cờ --dangerously-skip-permissions. Multica gọi CLI này bằng quyền user trên máy, không có sandbox, nên agent chạy được mọi lệnh. Đây là điểm phải xử lý nếu dùng thật, và được ghi trong báo cáo spike.
**Bài học:** Khi spike một agent chạy trên máy, kiểm alias và biến môi trường của shell, vì chúng có thể âm thầm mở quyền rộng hơn bạn nghĩ.
**Artefact:** Không cần chụp. Mô tả dòng alias là đủ.
