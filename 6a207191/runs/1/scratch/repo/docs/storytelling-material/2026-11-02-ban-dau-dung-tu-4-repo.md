---
id: 2026-11-02-ban-dau-dung-tu-4-repo
date: 2026-11-02
repo: repo
status: raw
signals: [số trước/sau, đảo quyết định]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:6a207191#L5", "claude:6a207191#L47", "claude:6a207191#L317", "claude:6a207191#L319", "claude:6a207191#L538"]
hook: "Bị chê dư thừa, agent cắt 11.900 chữ xuống 6.400"
tension: it_ma_nhieu
sides: ["Bản đầu 13 file, mỗi rule kèm 2 đến 6 dòng giải thích", "Mỗi rule một dòng, giảm 46% chữ mà lint vẫn qua 190 rule"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Bản đầu dựng từ 4 repo gần gấp đôi, cắt bớt 46% chữ sau khi bị chê dư thừa

**Bối cảnh:** Mục tiêu là gom cách làm packaging và distribution (install, update, config, doctor) của 4 repo thành một skill dùng lại cho các dự án sau. Bốn agent con đọc song song 4 repo rồi agent chính dựng skill.
**Chuyện gì xảy ra:** Bản đầu có 13 file common, mỗi rule có tiêu đề riêng và 2 đến 6 dòng giải thích, tổng khoảng 11.900 từ. Người dùng nhận xét là dư thừa. Agent sao lưu bản cũ rồi viết lại: mỗi rule còn một dòng, bỏ 4 file case study thay bằng một bảng references.md trỏ thẳng tới code trong repo, và bỏ các rule trùng nhau. Kết quả khoảng 6.400 từ (giảm 46%) và script lint vẫn qua với 190 rule.
**Bài học:** Đo số từ của bộ hướng dẫn ngay từ bản đầu, và để mỗi rule trỏ về ví dụ code thật thay vì giải thích lại.
**Artefact:** Bảng so trước/sau theo số từ từng thư mục, kèm ảnh một rule trước (3 dòng) và sau (1 dòng). Không chụp đường dẫn máy.
