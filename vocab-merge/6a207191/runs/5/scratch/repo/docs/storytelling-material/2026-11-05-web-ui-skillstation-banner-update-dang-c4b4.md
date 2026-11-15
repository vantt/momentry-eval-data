---
id: 2026-11-05-web-ui-skillstation-banner-update-dang-c4b4
code: M-ETKX
aliases: [M-ETKX]
date: 2026-11-05
repo: repo
status: raw
signals: [artefact, số trước/sau]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:6a207191#L1745", "claude:6a207191#L1872", "claude:6a207191#L1976", "claude:6a207191#L1980", "claude:6a207191#L1988", "claude:6a207191#L2008", "claude:6a207191#L2080", "claude:6a207191#L2103"]
hook: "229 test xanh, merge thẳng main, nhưng chưa mở trình duyệt lần nào"
tension: tuong_ma_hoa_ra
sides: ["229 test, tsc, eslint, build đều qua", "chưa ai mở giao diện trên trình duyệt thật"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Web UI skillstation: banner update đang chờ duyệt, 229 test qua, merge thẳng vào main

**Bối cảnh:** Khi bản gửi từ máy khác cho một skill đã có trên hub, nó chỉ hiện ở Waiting for review; trang skill không báo gì.
**Chuyện gì xảy ra:** Agent thêm 4 file mới và sửa 6 file: banner trên trang skill có nút Review it, nhãn Update waiting for review trong danh sách, và nhãn Older cho bản gửi cũ hơn. Mã SUB có thứ tự theo thời gian nên được dùng để tìm bản mới nhất. Một lỗi TypeScript strict được sửa, sau đó 229 test web, tsc, eslint và build đều qua. Chưa mở trình duyệt thật. Theo yêu cầu người dùng, agent merge fast-forward vào main và push, không mở PR.
**Bài học:** Khi thêm trạng thái chờ, hiển thị nó ngay trên đối tượng đang xem thay vì để người xem tự tìm ở danh sách khác.
**Artefact:** Ảnh banner 'An update to this skill is waiting for review' và nút Review it. Cần che mã SUB và tên máy.
