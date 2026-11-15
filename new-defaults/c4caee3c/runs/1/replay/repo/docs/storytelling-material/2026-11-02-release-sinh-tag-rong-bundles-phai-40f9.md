---
id: 2026-11-02-release-sinh-tag-rong-bundles-phai-40f9
code: M-VB4P
aliases: [M-VB4P]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L2986", "claude:c4caee3c#L2988", "claude:c4caee3c#L3001", "claude:c4caee3c#L3029", "claude:c4caee3c#L3370"]
hook: "Release ra tag rỗng, phải tự tay chạy bundles cho đến khi nối được"
tension: cam_ma_van_lot
sides: ["Quy trình release đã tự động", "Tag vantt.2 ra rỗng, bundles phải dispatch tay"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Release sinh tag rỗng, bundles phải nối tay đến khi catchup gọi bundles

**Bối cảnh:** Catchup đẩy tag vantt.2 trước khi workflow bundles được nối vào.
**Chuyện gì xảy ra:** Release vantt.2 xuất hiện rỗng, lượt bundles của nó hỏng ở bước so mức lệch cũ, agent phải dispatch bundles bằng tay. Sau đó catchup được nối với bước dựng gói, và vantt.3 có đủ 12 file tự động.
**Bài học:** Nối các bước phát hành thành một chuỗi trước khi bật tự động; release rỗng là dấu hiệu chuỗi đã đứt.
**Artefact:** Danh sách asset của release, chỉ tên file.
