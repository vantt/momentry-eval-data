---
id: 2026-11-05-trang-skill-khong-bao-co-ban
date: 2026-11-05
repo: repo
status: raw
signals: [đảo quyết định, khác]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:6a207191#L1489", "claude:6a207191#L1507", "claude:6a207191#L1515", "claude:6a207191#L1745", "claude:6a207191#L1808", "claude:6a207191#L1917", "claude:6a207191#L1976", "claude:6a207191#L1980", "claude:6a207191#L1988", "claude:6a207191#L2001", "claude:6a207191#L2008"]
hook: "Bản chờ duyệt nằm im, trang skill không báo gì; 229 test xanh nhưng chưa mở trình duyệt"
tension: tuong_ma_hoa_ra
sides: ["229 test web qua, tsc, eslint và build đều sạch", "Chưa mở trình duyệt thật lần nào"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Trang skill không báo có bản chờ duyệt: thêm banner và nhãn, 229 test web xanh

**Bối cảnh:** Hub đã kích hoạt bản skill cũ trong khi bản gửi mới nằm ở Waiting for review. Trang skill không báo gì nên người duyệt dễ duyệt nhầm bản cũ.
**Chuyện gì xảy ra:** Agent đề xuất sửa phía skillstation, người dùng yêu cầu làm bằng skill frontend. Agent thêm hàm chọn bản mới nhất theo mã SUB (sắp xếp được theo thời gian gửi), banner trên trang skill với nút Review và Discard older, nhãn Update waiting for review trong danh sách và nhãn Older trong hàng chờ. Lỗi TypeScript được sửa trong test, và một hook chặn lệnh grep đọc thư mục dist nên phải đi đường khác. Kết quả: 229 test web qua, tsc, eslint và build sạch, nhưng chưa mở trình duyệt thật.
**Bài học:** Trạng thái chờ duyệt phải hiện ở nơi người ta nhìn vào skill, không chỉ nằm trong một tab riêng.
**Artefact:** Chưa có ảnh. Cần chạy web thật để chụp banner trên trang skill và nhãn trong danh sách.
