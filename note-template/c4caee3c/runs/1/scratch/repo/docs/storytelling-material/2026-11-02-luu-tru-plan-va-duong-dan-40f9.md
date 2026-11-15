---
id: 2026-11-02-luu-tru-plan-va-duong-dan-40f9
code: M-PW8P
aliases: [M-PW8P]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
signal_note: "Đổi vị trí lưu plan kéo theo nhiều đường dẫn tham chiếu, và phải sửa từng chỗ."
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L3121", "claude:c4caee3c#L3132", "claude:c4caee3c#L3180", "claude:c4caee3c#L3198"]
hook: "Chuyển 25 plan vào archive, ba chỗ vẫn trỏ đường dẫn cũ"
tension: nho_ma_to
sides: ["Đã chuyển 25 plan vào archive", "Ba đường dẫn cũ còn sót"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Lưu trữ plan và đường dẫn cũ

**Bối cảnh:** Quy tắc của dự án: plan con xong thì chuyển vào archive.
**Chuyện gì xảy ra:** Hai mươi lăm plan con được chuyển vào archive. Ba chỗ còn trỏ đường dẫn cũ, và ba plan thiếu trạng thái phải bổ sung. Một số phase chưa xong vẫn giữ ở vị trí cũ.
**Bài học:** Khi chuyển tài liệu, tìm mọi tham chiếu đến đường dẫn cũ bằng grep trước khi commit.
