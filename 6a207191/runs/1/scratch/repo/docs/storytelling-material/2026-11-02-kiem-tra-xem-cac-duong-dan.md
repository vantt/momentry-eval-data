---
id: 2026-11-02-kiem-tra-xem-cac-duong-dan
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:6a207191#L282", "claude:6a207191#L423", "claude:6a207191#L527", "claude:6a207191#L533", "claude:6a207191#L855", "claude:6a207191#L856", "claude:6a207191#L2358", "claude:6a207191#L2364"]
hook: "Cố tình chèn ID sai vào tài liệu để thử xem script có bắt được không"
tension: khac
sides: ["Tài liệu viết xong thì để đó, đường dẫn hỏng dần không ai hay", "Chủ động chèn ID sai để kiểm tra chính bộ kiểm tra"]
strength: 2
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Kiểm tra xem các đường dẫn tới code mẫu trong tài liệu skill có thật không, bằng script đối chiếu với GitHub. Chủ động chèn một ID sai hoặc dải ID sai vào để xem script có bắt được lỗi không.

**Chuyện gì xảy ra:** Kiểm tra xem các đường dẫn tới code mẫu trong tài liệu skill có thật không, bằng script đối chiếu với GitHub. Chủ động chèn một ID sai hoặc dải ID sai vào để xem script có bắt được lỗi không.
**Góc người ngoài:** cách làm phổ biến là Tài liệu viết xong thì để đó. Đường dẫn trong docs hỏng dần mà không ai biết cho tới khi có người bấm vào. Hiếm ai viết lint cho chính tài liệu của mình; ở đây khác ở Skill được coi là 'bộ bí kiếp tích lũy lâu dài' nên cần chống mục nát. Có lint về cấu trúc (frontmatter, ID không trùng, tham chiếu chéo phải tồn tại) và một script riêng đối chiếu đường dẫn với repo thật. Việc cố tình làm hỏng thử để chứng minh script bắt được là mẹo hay mà người đọc muốn học.
