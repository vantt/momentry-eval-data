---
id: 2026-11-02-dat-ten-ho-skill-cs-de
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:6a207191#L695", "claude:6a207191#L697", "claude:6a207191#L701", "claude:6a207191#L735"]
hook: "Tên 'cs-' dễ bị đọc thành C#, nên phải giải nghĩa ngay đầu mô tả"
tension: nho_ma_to
sides: ["Tiền tố hai chữ cái cho gọn", "Agent đọc nhầm thành C#, mô tả phải giải nghĩa"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đặt tên họ skill: 'cs-' dễ bị đọc thành C#, nên mô tả mở đầu phải giải nghĩa

**Bối cảnh:** Người dùng muốn đặt tên họ skill để sau này có cs-architecture-quality, cs-test-quality.
**Chuyện gì xảy ra:** Agent đề xuất giữ 'distribution' thay vì 'installation' vì skill còn gồm release, update, config và tích hợp agent. So giữa 'cs-' và 'code-standard-' (dài 36 ký tự), chọn cs-packaging-distribution, đồng thời đưa 'Code standard (cs-*)' lên đầu mô tả vì agent chọn skill qua mô tả. Đổi tên thư mục và symlink trong cùng một lượt.
**Bài học:** Tiền tố viết tắt cần được giải nghĩa trong mô tả, vì agent chọn skill qua mô tả chứ không qua tên.
**Artefact:** Danh sách tên họ skill cho thấy tiền tố chung.
