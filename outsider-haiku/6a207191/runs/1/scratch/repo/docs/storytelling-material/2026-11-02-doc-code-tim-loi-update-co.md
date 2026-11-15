---
id: 2026-11-02-doc-code-tim-loi-update-co
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:6a207191#L96", "claude:6a207191#L957"]
hook: "Lệnh update có vẻ ghi file nén đè lên chính binary đang chạy"
tension: giup_ma_hai
sides: ["lệnh update để cập nhật bản mới", "có vẻ ghi .tar.gz đè lên binary, chưa chạy thử"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đọc code tìm lỗi update: có vẻ ghi file .tar.gz đè lên binary, chưa chạy thử

**Bối cảnh:** Trong lúc distill, agent đọc code herdr-go và thấy các chỗ có vẻ sai trong update và uninstall.
**Chuyện gì xảy ra:** Báo cáo nói lệnh update ghi file .tar.gz đè lên binary đang chạy thay vì giải nén chương trình bên trong. Lệnh gỡ cài mà installer macOS in ra lại trỏ tới một file không được publish. Agent kết luận từ đọc code, chưa chạy thử, và ghi rõ điều này trong báo cáo cuối.
**Bài học:** Ghi rõ bằng chứng là đọc code hay đã chạy. Một bug suy ra từ code chưa phải là bug đã được tái hiện.
**Artefact:** Chưa có. Nếu xác nhận được thì chụp output của lần chạy thử.
