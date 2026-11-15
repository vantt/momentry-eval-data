---
id: 2026-11-02-pre-push-hook-chan-push-va
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L204", "claude:c4caee3c#L209", "claude:c4caee3c#L220", "claude:c4caee3c#L800"]
hook: "Hook chặn push, nên lệnh sau đặt HUSKY=0 cho mọi lần push"
tension: cam_ma_van_lot
sides: ["Hook pre-push đã chặn lần push đầu", "Một biến môi trường tắt hook cho mọi lần push sau"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Pre-push hook chặn push và mẫu lệnh HUSKY=0 lặp lại

**Bối cảnh:** Repo có hook pre-push cài bằng husky, chạy test trước khi đẩy.
**Chuyện gì xảy ra:** Lệnh push đầu tiên thất bại vì hook; commit đã vào máy nhưng chưa lên origin. Lệnh sau đó đặt HUSKY=0 cho mọi lần push. Một lệnh pull --rebase cũng bị từ chối vì có thay đổi chưa commit, buộc phải autostash.
**Bài học:** Ghi lại vì sao hook chặn và sửa nguyên nhân; đặt biến tắt hook làm mất lưới an toàn âm thầm.
**Artefact:** Thông báo lỗi hook, đã bỏ đường dẫn.
