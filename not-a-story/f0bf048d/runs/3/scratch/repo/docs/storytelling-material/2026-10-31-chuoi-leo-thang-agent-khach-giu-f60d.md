---
id: 2026-10-31-chuoi-leo-thang-agent-khach-giu-f60d
code: M-GNK7
aliases: [M-GNK7]
date: 2026-10-31
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, rang_buoc_thiet_ke]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:f0bf048d#L1874", "claude:f0bf048d#L1891"]
hook: "Agent khách giữ PAT của chủ, giao việc được cho agent có docker gần như root"
tension: nho_ma_to
sides: ["Một PAT của chủ nằm trong daemon của agent khách", "Nó mở đường tới System Operator có nhóm docker, gần như quyền root"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chuỗi leo thang: agent khách giữ PAT chủ, giao việc cho System Operator có docker

**Bối cảnh:** Bản phản biện chỉ ra cách một agent bị điều khiển có thể đi tới quyền root trên máy.
**Chuyện gì xảy ra:** Daemon của agent khách đăng nhập bằng PAT của chủ, nên agent có thể giao việc cho System Operator. System Operator chạy dưới user có nhóm docker, tức gần như root. Daemon spike cũng chạy agent khác dưới cùng user. Thứ tự xử lý: dừng daemon đang rảnh, tắt mã dev, đổi daemon sang danh tính riêng, thu hồi PAT chủ.
**Bài học:** Đừng để agent chạy bằng token của chủ. Một chuỗi từ agent tới đặc quyền thường nằm ở một chỗ không ai nghi.
**Artefact:** Sơ đồ chuỗi leo thang dạng văn bản.
**Góc người ngoài:** cách làm phổ biến là Thường dặn agent trong prompt là đừng làm việc nguy hiểm, và dùng chung một token admin cho mọi tiến trình tự động; ở đây khác ở Phiên này coi lời dặn không đáng tin khi có prompt injection, nên cắt đường leo quyền bằng quyền hệ điều hành, danh tính Multica và không quyền ghi. Người đọc cần biết vì sao làm như vậy và cái giá là phải kéo bản vá về bằng tay.
