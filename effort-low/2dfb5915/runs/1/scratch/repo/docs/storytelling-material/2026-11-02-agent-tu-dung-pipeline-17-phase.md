---
id: 2026-11-02-agent-tu-dung-pipeline-17-phase
date: 2026-11-02
repo: repo
status: raw
signals: [artefact nhìn được, ràng buộc định hình thiết kế]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L11", "claude:2dfb5915#L120", "claude:2dfb5915#L178", "claude:2dfb5915#L1017", "claude:2dfb5915#L1224"]
hook: "17 phase Rust, 7 agent chạy song song, 64 mục so khớp, 0 lệch"
tension: hop_ma_tan
sides: ["Nhiều agent chạy song song, CI xanh trên cả ba hệ điều hành", "Merge vẫn xung đột ở spec và Cargo.lock, phải gỡ tay"]
strength: 1
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent tự dựng pipeline 17 phase Rust cho bản Python, chạy song song bằng nhiều agent

**Bối cảnh:** Người dùng giao một plan port core Python sang Rust (17 phase). Lead agent bật nhiều subagent làm song song, mỗi agent có worktree riêng, rồi merge từng nhánh về main.
**Chuyện gì xảy ra:** Wave đầu gồm 7 phase chạy đồng thời; CI xanh trên Linux, macOS và Windows sau mỗi lần merge. Bộ so khớp với Python ra 64 mục, 0 lệch. Nhiều lần merge xung đột ở spec/PORTING.md và Cargo.lock, phải gỡ tay và merge lại.
**Bài học:** Chạy song song nhiều agent cần một bộ so khớp tự động với bản gốc; không có nó thì không biết agent nào sai.
**Artefact:** Bảng tiến độ phase, số mục khớp/lệch từ bộ so khớp; che tên vault và đường dẫn.
**Góc người ngoài:** cách làm phổ biến là Phần lớn dev dùng AI theo kiểu hỏi-đáp từng lượt: đưa một việc nhỏ, đọc kết quả, sửa, rồi làm tiếp. Việc nhiều nhánh song song thường do người tự điều phối, mở nhiều cửa sổ chat hoặc tự chia branch; ở đây khác ở Ở đây agent tự quyết cách chia việc, mở và thu hồi nhiều agent con, xử lý xung đột merge, rồi dừng khi điều kiện chưa đạt. Người đọc sẽ hỏi làm sao để một lần giao việc mà không cần ngồi canh từng bước, và điều gì giữ cho các nhánh song song không dẫm lên nhau.
