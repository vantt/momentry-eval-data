---
id: 2026-11-02-khi-nhan-cau-hoi-cua-nguoi
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:c4caee3c#L2237", "claude:c4caee3c#L2255", "claude:c4caee3c#L2450", "claude:c4caee3c#L2466", "claude:c4caee3c#L2502", "claude:c4caee3c#L2508", "claude:c4caee3c#L2514", "claude:c4caee3c#L2526"]
hook: "Trả lời xong còn đối chiếu PRD, sai thì sửa ngay trong commit"
tension: none
sides: []
strength: 0
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Khi nhận câu hỏi của người dùng về một khái niệm (L13, L22, L15, L24), agent trả lời ngắn, tách rõ phần nào thuộc repo nào, sau đó đối chiếu với PRD trước khi khẳng định, và sửa nhầm lẫn của chính mình ngay trong commit.

**Chuyện gì xảy ra:** Khi nhận câu hỏi của người dùng về một khái niệm (L13, L22, L15, L24), agent trả lời ngắn, tách rõ phần nào thuộc repo nào, sau đó đối chiếu với PRD trước khi khẳng định, và sửa nhầm lẫn của chính mình ngay trong commit.
**Góc người ngoài:** cách làm phổ biến là Thường AI trả lời tự tin mà không đối chiếu tài liệu, hoặc giải thích dài dòng; khi sai thì không sửa lại tài liệu; ở đây khác ở Agent tự nhận sai khi ghi nhầm dòng PRD, kiểm lại bằng git show, sửa trong cùng commit, và luôn trích mục PRD cụ thể làm căn cứ. Người đọc muốn biết cách bắt lỗi của chính AI trước khi người khác phát hiện.
