---
id: 2026-10-29-commit-dung-phan-cua-minh-giu-c455
code: M-32SS
aliases: [M-32SS]
date: 2026-10-29
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:0faf0bb2#L2166", "claude:0faf0bb2#L2172", "claude:0faf0bb2#L2176", "claude:0faf0bb2#L2184", "claude:0faf0bb2#L2191", "claude:0faf0bb2#L3916", "claude:0faf0bb2#L3924", "claude:0faf0bb2#L3927"]
hook: "Commit 20 file mà không đụng tới một dòng dở của người khác"
tension: it_ma_nhieu
sides: ["Thao tác git thông thường dễ cuốn theo thay đổi dở", "Index riêng chỉ đưa đúng các file tài liệu và hai dòng README"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Commit đúng phần của mình, giữ nguyên thay đổi dở của người khác

**Bối cảnh:** Repo có sẵn thay đổi dở ở thư mục company, kể cả phần đã stage.
**Chuyện gì xảy ra:** Thay vì add và commit thông thường, tạo index riêng bằng GIT_INDEX_FILE để chỉ đưa vào commit các file tài liệu và đúng hai dòng README. Commit c7181d6 có 20 file, +3.257 dòng. Commit 152f378 sau đó có 14 file. Phần dở của người khác không bị đụng tới. Lần thứ hai cũng làm theo cách này.
**Bài học:** Khi repo có thay đổi dở không phải của mình, dùng index riêng để commit đúng phần. Không dùng reset hay stash chung.
**Artefact:** Kết quả git log --stat của c7181d6 và 152f378. Không có gì cần che.
