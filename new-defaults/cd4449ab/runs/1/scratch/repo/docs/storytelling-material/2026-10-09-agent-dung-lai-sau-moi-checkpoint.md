---
id: 2026-10-09-agent-dung-lai-sau-moi-checkpoint
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [outsider]
lines: ["omp:cd4449ab#L2025", "omp:cd4449ab#L2122", "omp:cd4449ab#L2344", "omp:cd4449ab#L2373", "omp:cd4449ab#L2374"]
hook: "Agent dừng sau mỗi checkpoint, chờ lead gật đầu mới đi tiếp"
tension: none
sides: []
strength: 0
stakes: 0
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent dừng lại sau mỗi checkpoint, báo hash commit và chờ lead xác nhận (merge, rebase, cho phép đi tiếp) trước khi làm phần tiếp theo.

**Chuyện gì xảy ra:** Agent dừng lại sau mỗi checkpoint, báo hash commit và chờ lead xác nhận (merge, rebase, cho phép đi tiếp) trước khi làm phần tiếp theo.
**Góc người ngoài:** cách làm phổ biến là Thường agent làm liền một mạch tới hết task, rồi báo một lần ở cuối. Ít ai dừng giữa chừng để chờ người khác duyệt; ở đây khác ở Ở đây có nhiều agent chạy song song trên các worktree, và lead là người duy nhất merge vào main. Điểm dừng được đặt có chủ đích để tránh một agent đi trước và làm vỡ agent khác. Người đọc sẽ muốn biết cách phối hợp kiểu này được thiết lập ra sao.
