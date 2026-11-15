---
id: 2026-11-02-release-rong-do-workflow-tu-tao-40f9
code: M-Y5E9
aliases: [M-Y5E9]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
signal_note: "Workflow tạo release trước khi các gói được dựng xong, nên release rỗng hiện ra như bản mới nhất."
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L2986", "claude:c4caee3c#L2988", "claude:c4caee3c#L3001", "claude:c4caee3c#L3029", "claude:c4caee3c#L3036"]
hook: "Release vantt.2 xuất hiện với 0 file dù bốn gói đã dựng xong"
tension: tuong_ma_hoa_ra
sides: ["Bốn gói đều dựng xong", "Release trống vì chạy trước khi sửa điều kiện"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Release rỗng do workflow tự tạo trước khi có gói

**Bối cảnh:** Catchup tự tạo release khi có tag mới và gọi bước dựng gói sau đó.
**Chuyện gì xảy ra:** Release vantt.2 xuất hiện với 0 file trong khi gói đang dựng. Lượt dựng đầu chạy trước khi sửa điều kiện so sánh, nên thất bại dù cả bốn gói đều dựng xong. Agent phải chạy lại thủ công. Sau đó cả bốn gói đã có kèm sha256.
**Bài học:** Chỉ tạo release khi có đủ artifact, hoặc đánh dấu release là nháp cho đến khi xong.
