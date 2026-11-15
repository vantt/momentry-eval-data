---
id: 2026-11-02-khi-hai-agent-cung-sua-cac
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:2dfb5915#L403", "claude:2dfb5915#L411", "claude:2dfb5915#L719", "claude:2dfb5915#L957", "claude:2dfb5915#L1208", "claude:2dfb5915#L1488", "claude:2dfb5915#L1901"]
hook: "Bảy agent chạy song song trên một repo, không cãi nhau vì một script merge"
tension: khac
sides: ["Nhiều agent cùng sửa một repo thường đẻ ra xung đột", "Một script ngắn giải xong, merge sạch rồi mới push"]
strength: 2
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Khi hai agent cùng sửa các file dùng chung (PORTING.md, DECISIONS.md, Cargo.lock), lead merge từng nhánh worktree và giải xung đột bằng script ngắn (giữ cả hai phía với file nhật ký, tạo lại lockfile), rồi chạy lại fmt, clippy, test và parity trước khi push.

**Chuyện gì xảy ra:** Khi hai agent cùng sửa các file dùng chung (PORTING.md, DECISIONS.md, Cargo.lock), lead merge từng nhánh worktree và giải xung đột bằng script ngắn (giữ cả hai phía với file nhật ký, tạo lại lockfile), rồi chạy lại fmt, clippy, test và parity trước khi push.
**Góc người ngoài:** cách làm phổ biến là Chạy một agent tại một thời điểm, hoặc để agent tự rebase rồi cãi nhau với conflict. Nhiều người không dám chạy nhiều agent song song trên cùng repo; ở đây khác ở Thiết kế để các file 'chỉ nối thêm' thì conflict giải được máy móc. Mỗi lần merge đều chạy lại toàn bộ cổng kiểm. Nhờ vậy 4 agent song song mà main vẫn xanh. Người đọc muốn biết cách chia việc để chạy song song mà không vỡ.
