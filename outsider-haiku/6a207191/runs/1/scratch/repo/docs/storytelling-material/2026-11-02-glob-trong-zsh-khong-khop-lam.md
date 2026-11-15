---
id: 2026-11-02-glob-trong-zsh-khong-khop-lam
date: 2026-11-02
repo: repo
status: raw
signals: [khác, nguyên nhân bất ngờ]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:6a207191#L423", "claude:6a207191#L424", "claude:6a207191#L434", "claude:6a207191#L435", "claude:6a207191#L856"]
hook: "File có thật nhưng bị báo thiếu, vì zsh không mở được dấu *"
tension: tuong_ma_hoa_ra
sides: ["báo MISSING", "file vẫn nằm đó, chỉ là glob không khớp"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Glob trong zsh không khớp làm kiểm tra đường dẫn báo thiếu file

**Bối cảnh:** Kiểm tra đường dẫn tham chiếu của skill được chạy trong shell zsh trên máy này.
**Chuyện gì xảy ra:** Lệnh grep với --include=*.go báo 'no matches found' vì zsh báo lỗi khi glob không khớp, khác với bash. Một đường dẫn có dấu * trong tài liệu bị đánh dấu MISSING vì bản kiểm tra không mở rộng được glob. Agent sửa đường dẫn thành tên file thật, sau đó check-references.sh chạy qua và xác nhận mọi đường dẫn có thật.
**Bài học:** Chạy các lệnh kiểm tra bằng sh cố định, không phụ thuộc shell tương tác. Glob không khớp trong zsh là lỗi hay gặp.
**Artefact:** Hai dòng 'no matches found' và danh sách MISSING trước khi sửa.
