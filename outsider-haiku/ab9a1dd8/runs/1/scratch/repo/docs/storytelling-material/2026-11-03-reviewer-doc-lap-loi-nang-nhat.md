---
id: 2026-11-03-reviewer-doc-lap-loi-nang-nhat
date: 2026-11-03
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, người duyệt]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2026", "claude:ab9a1dd8#L2039", "claude:ab9a1dd8#L2058", "claude:ab9a1dd8#L2062", "claude:ab9a1dd8#L2079"]
hook: "Reviewer tìm 16 lỗi; lỗi nặng nhất chỉ là một cặp nháy kép"
tension: nho_ma_to
sides: ["một cặp dấu ngoặc kép", "installer luôn báo Node quá cũ"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Reviewer độc lập: lỗi nặng nhất là một cặp dấu ngoặc

**Bối cảnh:** Code và test đã xanh 230/230 trên Linux, nhưng nhánh Windows chưa ai chạy thật. Một subagent review đọc code để tìm lỗi.
**Chuyện gì xảy ra:** Reviewer báo 4 lỗi nặng, 5 trung bình và 7 nhẹ. Lỗi nặng nhất: lệnh node -p dùng dấu nháy kép lồng trong PowerShell 5.1, Node nhận split(.) và installer luôn báo Node quá cũ. Lỗi thứ hai: lệnh xoá qua cmd không hiểu escape nên không xoá gì nhưng vẫn báo thành công. Lỗi thứ ba: trên Windows cache nằm trong thư mục cài nên uninstall thông thường sẽ xoá dữ liệu người dùng.
**Bài học:** Lỗi nặng hay nằm ở dấu nháy; test trên Linux không bắt được, nên phải chạy thật trên hệ đó.
**Artefact:** Dòng code gây lỗi dấu nháy trước và sau khi sửa.
