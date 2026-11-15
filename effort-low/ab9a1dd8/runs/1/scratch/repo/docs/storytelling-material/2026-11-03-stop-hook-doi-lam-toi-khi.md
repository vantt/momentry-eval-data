---
id: 2026-11-03-stop-hook-doi-lam-toi-khi
date: 2026-11-03
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2233", "claude:ab9a1dd8#L2948", "claude:ab9a1dd8#L3047"]
hook: "45/45 việc xong, mà hook vẫn trả về ba lần"
tension: tuong_ma_hoa_ra
sides: ["45/45 việc trong plan đã xong", "stop hook vẫn bắt làm tiếp ba lần"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Stop hook đòi làm tới khi tốt đẹp: 45/45 việc chưa đủ

**Bối cảnh:** Điều kiện của phiên là làm plan tới khi hoàn tất tốt đẹp. Agent đã đánh dấu 45/45 việc, nhưng vẫn còn việc chưa đo được ngoài môi trường hiện tại.
**Chuyện gì xảy ra:** Ba lần stop hook trả lại việc. Lần đầu là hai việc cần push. Lần hai là release chưa cắt và hook Windows chưa đo. Lần ba là hook Windows chưa đo trong phiên thật. Agent xử lý từng cái: hỏi người trước các việc công khai, mở issue cho phần không làm được ngay.
**Bài học:** Đánh dấu xong trong plan không đồng nghĩa với xong; với việc không làm được trong môi trường này, ghi rõ phần còn lại và theo dõi bằng issue.
**Artefact:** Bảng ba lần stop hook với điều kiện và việc còn lại tương ứng. Không cần che gì.
