---
id: 2026-11-02-agent-review-doc-lap-bat-duoc-c4b4
code: M-CKX6
aliases: [M-CKX6]
date: 2026-11-02
repo: repo
status: raw
signals: [nguoi_duyet_may_soan, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:6a207191#L296", "claude:6a207191#L300", "claude:6a207191#L673", "claude:6a207191#L690"]
hook: "Reviewer độc lập bắt được installer vi phạm chính luật của nó"
tension: tuong_ma_hoa_ra
sides: ["Installer mẫu do chính bộ luật viết ra", "Nó vi phạm luật đó, chặn cả việc gỡ cài đặt"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent review độc lập bắt được chính skill mâu thuẫn và installer vi phạm luật của nó

**Bối cảnh:** Sau khi có skill, chủ dự án nhờ một agent mạnh đọc lại theo mục tiêu UX và agent-native, đóng vai agent được giao làm packaging cho một Go CLI có MCP server.
**Chuyện gì xảy ra:** Reviewer đưa ra 9 phát hiện, xếp theo mức độ. Một quy tắc bảo dùng lệnh setup, quy tắc khác nói không có setup. Chuỗi lệnh init --yes rồi doctor --fix --yes không bao giờ chạy connect, nên agent chỉ đọc --help sẽ không đăng ký MCP. Installer mẫu còn bị chặn khi gỡ cài đặt vì kiểm tra version chạy trước nhánh uninstall.
**Bài học:** Đưa skill cho một reviewer độc lập đọc theo mục tiêu sản phẩm. Mâu thuẫn giữa các file thường chỉ lộ ra khi có người đi hết quy trình.
**Artefact:** Danh sách 9 phát hiện theo mức độ. Không có thông tin cần che.
