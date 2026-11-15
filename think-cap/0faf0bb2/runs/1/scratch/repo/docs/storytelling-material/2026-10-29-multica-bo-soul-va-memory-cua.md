---
id: 2026-10-29-multica-bo-soul-va-memory-cua
date: 2026-10-29
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, nguyên nhân bất ngờ]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:0faf0bb2#L2104", "claude:0faf0bb2#L2105", "claude:0faf0bb2#L2111", "claude:0faf0bb2#L2126", "claude:0faf0bb2#L2410"]
hook: "Agent có linh hồn và trí nhớ, nhưng Multica đặt nó vào thư mục trống"
tension: tuong_ma_hoa_ra
sides: ["Agent OpenClaw có SOUL.md và MEMORY.md riêng", "Chạy local thì workspace bị thay, hai file đó bị loại"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Multica bỏ SOUL và MEMORY của agent OpenClaw khi chạy local

**Bối cảnh:** Đọc code daemon của Multica để xem agent OpenClaw được chạy như thế nào trước khi ghép với AICoworker.
**Chuyện gì xảy ra:** Trước mỗi lượt, daemon đặt workspace của agent OpenClaw thành thư mục riêng của task. Comment trong code ghi rõ SOUL.md và MEMORY.md của workspace gốc bị loại trừ. Chế độ gateway có thể giữ được danh tính, nhưng token ghi ngược có thể không tới được agent. Đây là chỗ hai hệ thống xung đột về nơi đặt bộ nhớ.
**Bài học:** Khi ghép hai hệ agent, kiểm tra xem hệ điều phối có ghi đè nơi lưu danh tính và bộ nhớ của agent hay không, trước khi viết adapter.
**Artefact:** Bảng hai chế độ local và gateway: cái gì giữ được, cái gì mất.
