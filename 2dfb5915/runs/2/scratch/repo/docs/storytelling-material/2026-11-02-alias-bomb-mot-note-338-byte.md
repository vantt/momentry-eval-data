---
id: 2026-11-02-alias-bomb-mot-note-338-byte
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, số trước sau]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L811", "claude:2dfb5915#L833"]
hook: "Một note 338 byte ngốn 1,45 GB RAM"
tension: nho_ma_to
sides: ["note chỉ 338 byte", "chiếm 1,45 GB RAM"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Alias bomb: một note 338 byte làm RSS lên 1,45 GB

**Bối cảnh:** Reviewer thử YAML độc hại trên bản Rust vừa merge.
**Chuyện gì xảy ra:** Note 338 byte với 7 tầng alias tạo 11,1 triệu prop và chiếm 1,45 GB RAM. Thêm một tầng là khoảng 14 GB. Python cũng phình (877 MB) nên đúng spec, nhưng vẫn là lỗ hổng DoS. Fix đặt ngân sách 1 triệu prop và 64 MiB text cho mỗi note. Vượt ngưỡng thì note đó ghi lỗi MemoryError và được ghi nhận là lệch có chủ ý.
**Bài học:** Khi đọc định dạng có alias hay merge, đặt giới hạn tài nguyên ngay từ đầu, vì kích thước input không cho biết kích thước sau khi mở rộng.
**Artefact:** Bảng kích thước input và RSS. Không cần chụp.
