---
id: 2026-11-02-cau-co-dau-giu-view-tat-40f9
code: M-GYSS
aliases: [M-GYSS]
date: 2026-11-02
repo: repo
status: raw
signals: [dao_quyet_dinh, khac]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L1264", "claude:c4caee3c#L2095", "claude:c4caee3c#L2096", "claude:c4caee3c#L2129", "claude:c4caee3c#L2160"]
hook: "Thay vì làm đúng PRD, họ giữ cách làm và sửa PRD"
tension: chon_mot_mat_mot
sides: ["Làm đúng PRD 10.3 như đã viết", "Giữ view tắt của V13 và sửa PRD cho khớp"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Câu có dấu: giữ view tắt và sửa PRD thay vì làm đúng PRD

**Bối cảnh:** PRD 10.3 ghi câu có dấu vẫn chạy cả view norm lẫn fold. Agent đã tắt, vì bật lên thì vi-semantic tụt 0,083 nDCG@5.
**Chuyện gì xảy ra:** Lead đề xuất giữ cách của V13 và sửa PRD 10.3 cho khớp. Người dùng chọn đúng phương án này sau một câu hỏi lựa chọn. Hai tuỳ chọn accentedNorm và accentedFold vẫn còn để bật lại khi cần.
**Bài học:** Khi một thay đổi làm hỏng một hạng mục, đo đánh đổi rồi để người duyệt chọn. Sau đó sửa tài liệu cho khớp quyết định thật.
