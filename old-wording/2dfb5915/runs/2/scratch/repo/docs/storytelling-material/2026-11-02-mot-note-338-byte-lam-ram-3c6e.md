---
id: 2026-11-02-mot-note-338-byte-lam-ram-3c6e
code: M-JR7N
aliases: [M-JR7N]
date: 2026-11-02
repo: repo
status: raw
signals: [khac, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L811", "claude:2dfb5915#L833"]
hook: "Một note 338 byte ngốn 1,45 GB RAM"
tension: nho_ma_to
sides: ["Note chỉ 338 byte, nhỏ hơn một tin nhắn", "Nó nở ra 11,1 triệu props và 1,45 GB RAM"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Một note 338 byte làm RAM lên 1,45 GB: bom alias YAML

**Bối cảnh:** Review code phát hiện YAML có alias lồng nhau gây bùng nổ bộ nhớ, cả Rust lẫn Python đều dính.
**Chuyện gì xảy ra:** Note 338 byte với 7 tầng alias tạo 11,1 triệu props và chiếm 1,45 GB RAM trong Rust. Thêm một tầng nữa (vẫn dưới 400 byte) cần khoảng 14 GB. Agent đặt ngân sách mỗi note là 1 triệu props và 64 MiB, vượt thì báo lỗi MemoryError và ghi như một lệch có chủ ý.
**Bài học:** Với đầu vào không tin cậy, một đoạn văn bản nhỏ có thể nhân lên thành dữ liệu rất lớn. Cần giới hạn ngân sách ngay từ đầu.
**Artefact:** Số liệu theo từng tầng alias (không có nội dung note).
