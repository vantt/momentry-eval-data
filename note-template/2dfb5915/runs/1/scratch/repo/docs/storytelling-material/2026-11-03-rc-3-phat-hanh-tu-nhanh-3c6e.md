---
id: 2026-11-03-rc-3-phat-hanh-tu-nhanh-3c6e
code: M-1GDX
aliases: [M-1GDX]
date: 2026-11-03
repo: repo
status: raw
signals: [dao_quyet_dinh]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L3717", "claude:2dfb5915#L3723", "claude:2dfb5915#L3881"]
hook: "Phát hành rc.3 từ nhánh chưa merge, main vẫn ở rc.2"
tension: khac
sides: ["Bản phát hành mới nhất là rc.3", "Nhánh chính vẫn đứng ở rc.2"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "Công cụ dòng lệnh cho vault Obsidian, có thêm cửa MCP để hỏi Claude Desktop về graph của vault; đang viết lại lõi bằng Rust."
spine_context_lines: [profile]
spine_want: Muốn thử luôn bản một cửa của phase 17 trong lúc chờ tuần chạy song song.
spine_want_lines: ["claude:2dfb5915#L3717"]
spine_obstacle: Phase 17 chưa merge vào main; plan chỉ merge sau phase 16.
spine_obstacle_lines: ["claude:2dfb5915#L3709"]
spine_action: Đánh tag v0.1.0-rc.3 từ nhánh phase-17-one-door (commit 535bc55) và đẩy lên origin.
spine_action_lines: ["claude:2dfb5915#L3881"]
spine_outcome: "Workflow release được theo dõi đến khi xong; theo chuyện, CI xanh và đủ 7 file với checksum khớp."
spine_outcome_lines: ["claude:2dfb5915#L3889"]
completeness: 5
---

# rc.3 phát hành từ nhánh chưa merge theo lựa chọn của người dùng

**Bối cảnh:** Plan ghi phase 17 chỉ merge vào main sau tuần chạy song song phase 16.
**Chuyện gì xảy ra:** Người dùng chọn thử luôn bản một cửa nên agent đánh tag rc.3 từ nhánh phase 17. Các job CI đều xanh sau khi repo công khai, và release có đủ 7 file với checksum khớp. Main vẫn ở rc.2.
**Bài học:** Có thể ra bản thử từ nhánh riêng, nhưng ghi rõ nhánh nguồn trong release và plan.
