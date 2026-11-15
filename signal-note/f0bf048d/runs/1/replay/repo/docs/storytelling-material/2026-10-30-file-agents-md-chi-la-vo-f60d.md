---
id: 2026-10-30-file-agents-md-chi-la-vo-f60d
code: M-NKSD
aliases: [M-NKSD]
date: 2026-10-30
repo: repo
status: raw
signals: [rang_buoc_thiet_ke]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L168", "claude:f0bf048d#L270", "claude:f0bf048d#L320", "claude:f0bf048d#L498"]
hook: "AGENTS.md chỉ là vỏ, nội dung thật dài gấp đôi giới hạn"
tension: tuong_ma_hoa_ra
sides: ["file AGENTS.md trông như đã đủ", "bản gốc 14.343 ký tự, giới hạn 8000"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# File AGENTS.md chỉ là vỏ, nội dung thật vượt giới hạn 8000 ký tự

**Bối cảnh:** Muốn nhập hai vai trò SEO và analytics từ kho mẫu cộng đồng vào gói OPC.
**Chuyện gì xảy ra:** File AGENTS.md trong kho mẫu chỉ có link tới repo gốc. Bản gốc dài 14.343 và 15.388 ký tự, vượt giới hạn 8000 ký tự cho phần instructions của agent trên Multica. Agent giữ nguyên văn mỗi vai trò thành một skill, ghim commit và kèm file license. AGENTS.md chỉ gắn vai trò vào bối cảnh công ty.
**Bài học:** Khi nền tảng giới hạn độ dài instructions, đặt nội dung dài vào skill và giữ phần vai trò thật ngắn.
**Artefact:** Bảng số ký tự của từng bản gốc so với giới hạn 8000.
