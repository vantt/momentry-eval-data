---
id: 2026-11-02-chay-song-song-bang-agent-17-3c6e
code: M-Q6PC
aliases: [M-Q6PC]
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L63", "claude:2dfb5915#L120", "claude:2dfb5915#L178", "claude:2dfb5915#L474", "claude:2dfb5915#L917", "claude:2dfb5915#L2144"]
hook: "17 phase, 7 agent song song, nhưng việc 'chặn' hoá ra là chờ người"
tension: tuong_ma_hoa_ra
sides: ["hook tưởng còn việc để agent làm tiếp", "các mục còn lại đều chờ Windows hoặc người duyệt"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chạy song song bằng agent: 17 phase, merge từng cái, và cái 'chặn' thật ra là chờ người

**Bối cảnh:** Dự án port một lõi Python sang Rust theo plan 17 phase. Agent chính điều phối nhiều subagent chạy song song, mỗi cái một git worktree, rồi merge về main từng cái khi xong.
**Chuyện gì xảy ra:** Phase 01 chạy một mình, các phase W1 chạy song song (7 agent). Mỗi agent xong thì được review bởi agent khác, rồi merge và push. Hook dừng phiên liên tục chặn vì điều kiện 'hoàn tất toàn bộ plan', trong khi các mục còn lại đều chờ Windows hoặc người duyệt. Tổng cộng 4 rc phát hành, mỗi cái qua CI ba nền.
**Bài học:** Tách việc chạy song song theo worktree và để một agent khác review trước khi merge; nhưng đừng để điều kiện dừng yêu cầu việc mà chỉ người hoặc máy khác làm được.
**Artefact:** Bảng trạng thái phase (xong / đang chạy / chờ người) trong plan.md; che đường dẫn vault và tên repo nếu cần.
**Góc người ngoài:** cách làm phổ biến là Thường một người làm tuần tự từng nhánh feature, hoặc giao cho một agent làm cả chuỗi trong một phiên dài, merge cuối cùng; ở đây khác ở Lead tách việc theo phụ thuộc, chạy nhiều agent cùng lúc trên worktree tách biệt để không đụng file nhau, rồi tự xử lý xung đột merge và chạy lại kiểm tra sau mỗi lần merge. Người đọc sẽ hỏi làm sao tránh agent giẫm lên nhau.
