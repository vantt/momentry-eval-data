---
id: 2026-11-03-antigravity-stop-hook-chay-sau-moi
date: 2026-11-03
repo: repo
status: raw
signals: [người duyệt]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L3410", "claude:ab9a1dd8#L3426", "claude:ab9a1dd8#L3427", "claude:ab9a1dd8#L3433"]
hook: "Antigravity có hook Stop, nhưng nó chạy sau mỗi lượt chứ không phải cuối phiên"
tension: tuong_ma_hoa_ra
sides: ["Tên Stop gợi ý kết thúc phiên", "Thực tế chạy sau mỗi lượt và có thể chặn agent"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Antigravity: Stop hook chạy sau mỗi lượt, nên không gom chuyện ở đó

**Bối cảnh:** Ba host mới là pi, omp và Antigravity (agy). Mỗi host có cơ chế hook khác nhau.
**Chuyện gì xảy ra:** pi và omp có extension TypeScript với sự kiện kết thúc phiên. agy chỉ có SessionStart và Stop, trong đó Stop chạy sau mỗi lượt và có thể chặn agent đang chạy. Agent đưa hai lựa chọn; user chọn gom khi mở phiên sau và tự tìm mọi profile.
**Bài học:** Hook chạy sau mỗi lượt là cái bẫy về chi phí và độ trễ; nên đặt điểm gom muộn hơn, lúc phiên mở lại.
**Artefact:** Bảng sự kiện hook của bốn host.
