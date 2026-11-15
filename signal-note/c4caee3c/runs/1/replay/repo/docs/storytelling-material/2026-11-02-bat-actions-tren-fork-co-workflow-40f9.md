---
id: 2026-11-02-bat-actions-tren-fork-co-workflow-40f9
code: M-FAGE
aliases: [M-FAGE]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L264", "claude:c4caee3c#L267", "claude:c4caee3c#L275", "claude:c4caee3c#L276", "claude:c4caee3c#L289"]
hook: "Bật Actions trên fork rồi tắt 4 workflow nguy hiểm, lệnh tắt trả 403"
tension: cam_ma_van_lot
sides: ["Định tắt workflow nguy hiểm", "Lệnh tắt bị 403, phải bật trước"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Bật Actions trên fork có workflow upstream: bật rồi tắt 4 workflow nguy hiểm

**Bối cảnh:** Người dùng hỏi có nên bật Actions để tự chạy catchup khi upstream đổi. Fork có sẵn bốn workflow upstream có thể tự tạo tag hoặc release.
**Chuyện gì xảy ra:** Người dùng đồng ý bật. Lệnh tắt workflow trả 403 vì workflow không đang chạy. Sau khi bật Actions, không có lượt chạy nào kích hoạt và bốn workflow đều ở trạng thái tắt. Sau đó người dùng đổi sang theo upstream thủ công bằng tag ghim.
**Bài học:** Bật Actions trên fork kéo theo các workflow gốc; kiểm danh sách workflow trước khi bật.
**Artefact:** Danh sách workflow và trạng thái (không kèm tên tài khoản).
