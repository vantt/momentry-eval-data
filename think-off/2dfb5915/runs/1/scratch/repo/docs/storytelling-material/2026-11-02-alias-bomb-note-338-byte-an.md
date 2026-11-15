---
id: 2026-11-02-alias-bomb-note-338-byte-an
date: 2026-11-02
repo: repo
status: raw
signals: [số trước sau, nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L811", "claude:2dfb5915#L819"]
hook: "Note 338 byte ngốn 1.45 GB RAM chỉ nhờ 7 tầng alias"
tension: nho_ma_to
sides: ["một note chỉ 338 byte", "11.1 triệu props và 1.45 GB RAM"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Alias bomb: note 338 byte ăn 1.45 GB RAM

**Bối cảnh:** Review YAML của bản Rust tìm ra lỗ hổng từ chối dịch vụ.
**Chuyện gì xảy ra:** Một note 338 byte với 7 tầng alias tạo 11.1 triệu props và 1.45 GB RSS. Tầng thứ tám ước tính cần khoảng 14 GB. Python cũng có hành vi này nên đặc tả vẫn khớp, nhưng đó vẫn là lỗ hổng. Sửa bằng ngân sách mỗi note là 1 triệu props và 64 MiB. Vượt ngân sách thì ghi lỗi MemoryError và ghi nhận như sai lệch có chủ đích.
**Bài học:** Đặc tả khớp không có nghĩa là an toàn. Đặt trần tài nguyên cho mọi đầu vào do người dùng cung cấp.
**Artefact:** Biểu đồ RSS theo số tầng alias.
