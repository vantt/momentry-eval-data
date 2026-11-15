---
id: 2026-11-02-hieu-nham-ten-viec-python-bi
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L2302", "claude:c4caee3c#L2320", "claude:c4caee3c#L2430", "claude:c4caee3c#L2450", "claude:c4caee3c#L2459", "claude:c4caee3c#L2466"]
hook: "Hai việc trùng tên khiến người duyệt tưởng Python bị bỏ"
tension: tuong_ma_hoa_ra
sides: ["Tưởng L15 là bỏ script Python", "Thật ra là viết lại toàn bộ bằng Rust, hai việc khác nhau"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hiểu nhầm tên việc: Python bị bỏ và Rust bị viết lại

**Bối cảnh:** PRD có nhiều mục đánh số N và L, trong đó N13 ghi viết lại bằng Rust và V16 ghi chuyển script Python, nhưng tên gọi dễ lẫn.
**Chuyện gì xảy ra:** Người duyệt hỏi L15 có phải các script Python bị bỏ không; lead trả lời trước đó nhầm vì hai việc khác nhau. Sau đó PRD được sửa để ghi rõ viết lại toàn bộ OHS bằng Rust, khác với việc chuyển script Python của dự án. Tương tự, L13 và L22 được chuyển sang repo dự án thay vì fork.
**Bài học:** Mục đánh số trong PRD cần câu mô tả đủ rõ để không bị đọc thành việc khác.
**Artefact:** Đoạn PRD trước và sau khi sửa tên việc.
