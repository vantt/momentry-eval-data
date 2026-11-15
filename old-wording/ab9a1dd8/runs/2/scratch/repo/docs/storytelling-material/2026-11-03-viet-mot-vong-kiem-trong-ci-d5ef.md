---
id: 2026-11-03-viet-mot-vong-kiem-trong-ci-d5ef
code: M-M6G8
aliases: [M-M6G8]
date: 2026-11-03
repo: repo
status: raw
signals: []
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:ab9a1dd8#L1542", "claude:ab9a1dd8#L1545", "claude:ab9a1dd8#L1960", "claude:ab9a1dd8#L2230"]
hook: "Một agent chỉ đọc --help, tự cài tự sửa rồi báo số vòng"
tension: it_ma_nhieu
sides: ["Agent mới chỉ đọc --help và --json", "Tự cài, tự sửa tới khi sẵn sàng và đếm số vòng"]
strength: 1
stakes: 2
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Viết một vòng kiểm trong CI: một agent mới chỉ đọc --help và --json, tự cài và tự sửa công cụ tới khi đạt trạng thái sẵn sàng, rồi báo số vòng cần.

**Chuyện gì xảy ra:** Viết một vòng kiểm trong CI: một agent mới chỉ đọc --help và --json, tự cài và tự sửa công cụ tới khi đạt trạng thái sẵn sàng, rồi báo số vòng cần.
**Góc người ngoài:** cách làm phổ biến là Viết tài liệu cho người đọc, rồi kiểm bằng cách có người thật làm theo; ở đây khác ở Tài liệu được kiểm bằng chính đối tượng dự định dùng là agent. Vòng thử lộ ra các câu hướng dẫn không chạy được và được sửa thành lệnh cụ thể.
