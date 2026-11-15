---
id: 2026-11-03-hook-ghi-cung-duong-dan-node-d5ef
code: M-8ZGC
aliases: [M-8ZGC]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L236", "claude:ab9a1dd8#L1170"]
hook: "Nâng Node một lần, hook chết im lặng và không ai biết"
tension: nho_ma_to
sides: ["Hook ghi cứng đường dẫn Node, luôn thoát 0", "Nâng Node là hỏng mà không doctor nào phát hiện"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Momentry là công cụ nhặt chuyện đáng kể từ phiên làm việc với coding agent, và người làm đang chuẩn bị đóng gói để người mới cài được ngay. Cấu hình hook in ra ghi cứng đường dẫn Node, tưởng vậy là đủ, nhưng nâng Node là hook chết mà không công cụ nào báo, vì lệnh luôn thoát 0. Người làm đã đổi hook sang gọi qua một lệnh cố định, và ai dựa vào hook trong công cụ dòng lệnh cần biết chuyện này."
audience: dev dùng hook với Claude Code hay Codex và tự cài công cụ dòng lệnh
spine_context: Momentry nhặt những chuyện đáng kể từ phiên làm việc với coding agent. Người làm đang chuẩn bị đóng gói để người mới cài và chạy được ngay.
spine_context_lines: [profile]
spine_want: "Người mới đi từ con số 0 tới lần chạy đầu thành công bằng một lệnh cài đặt, và agent đọc --help là đủ để tự cài và sửa."
spine_want_lines: ["claude:ab9a1dd8#L42"]
spine_obstacle: Cấu hình hook in ra ghi cứng đường dẫn Node tuyệt đối; lệnh hook luôn thoát 0 nên lỗi không hiện ra.
spine_obstacle_lines: ["claude:ab9a1dd8#L236"]
spine_turn: Tưởng in đường dẫn tuyệt đối là đủ; hoá ra nâng Node là hook chết mà không công cụ nào báo.
spine_turn_lines: ["claude:ab9a1dd8#L236"]
spine_action: Đổi hook sang gọi qua lệnh cài sẵn (paths.prefix) thay vì đường dẫn Node cứng.
spine_action_lines: ["claude:ab9a1dd8#L1170", "claude:ab9a1dd8#L1171"]
spine_takeaway: Hook không nên ghi cứng đường dẫn runtime. Cho nó gọi qua một lệnh ổn định và có cách kiểm tra hook đang trỏ tới đâu.
spine_takeaway_lines: ["claude:ab9a1dd8#L236"]
completeness: 6
---

# Hook ghi cứng đường dẫn Node tuyệt đối: nâng Node là hook chết mà không ai biết

**Góc kể:** Momentry là công cụ nhặt chuyện đáng kể từ phiên làm việc với coding agent, và người làm đang chuẩn bị đóng gói để người mới cài được ngay. Cấu hình hook in ra ghi cứng đường dẫn Node, tưởng vậy là đủ, nhưng nâng Node là hook chết mà không công cụ nào báo, vì lệnh luôn thoát 0. Người làm đã đổi hook sang gọi qua một lệnh cố định, và ai dựa vào hook trong công cụ dòng lệnh cần biết chuyện này.
**Bối cảnh:** Cấu hình hook in ra cho Claude Code và Codex có đường dẫn node và bin tuyệt đối.
**Chuyện gì xảy ra:** Lệnh hook luôn thoát 0 nên lỗi im lặng. Nâng Node qua nvm hoặc fnm, hoặc chuyển thư mục clone, là hook hỏng và không có doctor nào phát hiện. Sửa bằng cách cài một lệnh momentry vào ~/.local/bin, để hook gọi qua tên lệnh đó nên không còn đường dẫn Node cứng.
**Bài học:** Hook không nên ghi cứng đường dẫn runtime. Cho nó gọi qua một shim ổn định, và có lệnh kiểm tra để báo hook đang trỏ tới đâu.
**Artefact:** Đoạn JSON hook trước và sau khi sửa. Che đường dẫn HOME.
