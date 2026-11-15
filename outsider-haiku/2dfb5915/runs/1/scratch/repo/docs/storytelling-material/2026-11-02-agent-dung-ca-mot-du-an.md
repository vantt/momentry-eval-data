---
id: 2026-11-02-agent-dung-ca-mot-du-an
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:2dfb5915#L11", "claude:2dfb5915#L62", "claude:2dfb5915#L120", "claude:2dfb5915#L178", "claude:2dfb5915#L189", "claude:2dfb5915#L572", "claude:2dfb5915#L1304"]
hook: "Bảy agent port Rust song song trong cùng một phiên"
tension: it_ma_nhieu
sides: ["Một phiên làm việc duy nhất", "17 phase port xong, 7 phase chạy song song"]
strength: 2
stakes: 3
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent dựng cả một dự án lớn (port core từ Python sang Rust) bằng cách bung nhiều agent chạy song song, mỗi agent làm một phase trong worktree riêng, rồi merge từng phần vào main sau khi tự kiểm.

**Chuyện gì xảy ra:** Agent dựng cả một dự án lớn (port core từ Python sang Rust) bằng cách bung nhiều agent chạy song song, mỗi agent làm một phase trong worktree riêng, rồi merge từng phần vào main sau khi tự kiểm.
**Góc người ngoài:** cách làm phổ biến là Thường một người hoặc một agent làm tuần tự trên một nhánh, merge khi xong, ít khi tách song song nhiều phần rồi gộp lại trong cùng một phiên; ở đây khác ở Người đọc sẽ hỏi làm sao tách được việc và tránh xung đột: phiên này dùng thứ tự phụ thuộc (phase nền chạy trước, các phase độc lập chạy song song) và merge từng agent một kèm chạy lại gate, nên ít bị vỡ nhau.
