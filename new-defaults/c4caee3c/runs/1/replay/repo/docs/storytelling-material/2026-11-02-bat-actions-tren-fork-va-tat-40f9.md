---
id: 2026-11-02-bat-actions-tren-fork-va-tat-40f9
code: M-JK7G
aliases: [M-JK7G]
date: 2026-11-02
repo: repo
status: raw
signals: [khac, rang_buoc_thiet_ke]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L268", "claude:c4caee3c#L275", "claude:c4caee3c#L276", "claude:c4caee3c#L288", "claude:c4caee3c#L302"]
hook: "Lệnh tắt workflow báo 403, nhưng cả bốn workflow đã tắt sẵn"
tension: tuong_ma_hoa_ra
sides: ["Lỗi 403 trông như tắt thất bại", "Kiểm lại thì cả bốn workflow upstream đã ở trạng thái tắt"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Bật Actions trên fork và tắt workflow upstream: lỗi im lặng 403

**Bối cảnh:** Người dùng yêu cầu bật Actions để catchup tự chạy. Repo fork có sẵn workflow của upstream.
**Chuyện gì xảy ra:** Agent bật Actions rồi cố tắt bốn workflow upstream. gh workflow disable báo 403 'not active' với một workflow. Kiểm lại: Actions đang bật, không có lượt chạy nào, bốn workflow upstream ở trạng thái tắt.
**Bài học:** Kiểm lại trạng thái sau mỗi lệnh đổi cấu hình; lệnh disable có thể lỗi âm thầm trên một workflow.
