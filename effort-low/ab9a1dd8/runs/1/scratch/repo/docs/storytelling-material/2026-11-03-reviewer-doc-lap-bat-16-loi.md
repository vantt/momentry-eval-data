---
id: 2026-11-03-reviewer-doc-lap-bat-16-loi
date: 2026-11-03
repo: repo
status: raw
signals: [số trước số sau, nguyên nhân bất ngờ]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2039", "claude:ab9a1dd8#L2049", "claude:ab9a1dd8#L2058", "claude:ab9a1dd8#L2062"]
hook: "Installer Windows luôn báo Node quá cũ, dù Node mới tinh"
tension: tuong_ma_hoa_ra
sides: ["máy có Node mới", "installer luôn đọc version là 0 vì lỗi quote"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Reviewer độc lập bắt 16 lỗi, trong đó có installer Windows luôn báo Node quá cũ

**Bối cảnh:** Sau khi viết xong packaging, một subagent review đọc code mà không chạy trên Windows, dựa trên kiến thức về PowerShell 5.1, cmd.exe và Node.
**Chuyện gì xảy ra:** Reviewer báo 4 lỗi nặng, 5 trung bình và 7 nhẹ. Lỗi nặng nhất: cách quote trong PowerShell 5.1 làm Node đọc split(.) thành lỗi cú pháp, nên version luôn là 0 và installer luôn báo Node quá cũ. Agent sửa hết trong phạm vi và thêm test cho các trường hợp mới.
**Bài học:** Viết lệnh node -p trong PowerShell phải thoát dấu nháy cẩn thận; tốt hơn là đặt đoạn JS vào file rồi gọi file đó.
**Artefact:** Bảng 16 phát hiện theo mức độ, cột trạng thái đã sửa. Không cần che gì.
