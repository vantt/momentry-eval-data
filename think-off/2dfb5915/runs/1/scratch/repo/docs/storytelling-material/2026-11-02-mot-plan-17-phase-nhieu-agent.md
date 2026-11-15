---
id: 2026-11-02-mot-plan-17-phase-nhieu-agent
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L62", "claude:2dfb5915#L120", "claude:2dfb5915#L178", "claude:2dfb5915#L189"]
hook: "17 phase chia nhiều agent song song, CI ba nền xanh ngay"
tension: none
sides: []
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Một plan 17 phase, nhiều agent song song, merge từng nhánh

**Bối cảnh:** Repo đặc tả Python cần port sang Rust theo plan 17 phase, trong đó nhiều phase độc lập nhau.
**Chuyện gì xảy ra:** Phase 01 (khung workspace) chạy một mình vì mọi phase khác phụ thuộc nó. Sau đó 7 phase W1 chạy song song, mỗi phase trong worktree riêng. Agent xong việc thì nhánh được review, merge vào main rồi push. CI xanh trên Linux, macOS và Windows ngay sau đợt merge đầu tiên.
**Bài học:** Chia plan theo phụ thuộc: phase nền chạy trước, phần còn lại song song trong worktree riêng, mỗi nhánh merge kèm bộ kiểm gate.
**Artefact:** Bảng phase với cột phụ thuộc và trạng thái. Không cần che tên phase.
**Góc người ngoài:** cách làm phổ biến là Thường người dùng AI chạy một phiên, chờ kết quả, rồi gõ tiếp; khi có nhiều việc thì làm tuần tự, hoặc mở nhiều cửa sổ rồi tự gộp bằng tay và giải xung đột; ở đây khác ở Người đọc sẽ hỏi làm sao để một plan 17 phase chạy được nhiều nhánh cùng lúc mà không dẫm chân nhau; phiên này tách theo worktree, gộp từng nhánh và xử lý xung đột Cargo.lock và tài liệu chung một cách có quy trình.
