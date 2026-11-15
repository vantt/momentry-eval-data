---
id: 2026-11-02-eval-vault-that-tong-tang-0
date: 2026-11-02
repo: repo
status: raw
signals: [số trước sau, người duyệt thứ máy soạn, đảo quyết định có lý do]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L3653", "claude:c4caee3c#L3680", "claude:c4caee3c#L3682", "claude:c4caee3c#L3797"]
hook: "Vault thật tăng tổng từ 0,600 lên 0,698, nhưng cổng hạng mục vẫn đỏ"
tension: hop_ma_tan
sides: ["Điểm tổng tăng gần 0,10", "Hai hạng mục tụt, vi-iy mất 0,26 vì một câu rơi khỏi top 5"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Eval vault thật: tổng tăng 0,600 lên 0,698 nhưng cổng hạng mục đỏ, người dùng quyết

**Bối cảnh:** 61 câu trên vault thật. Hạng mục chỉ có 2 đến 6 câu nên một câu rơi làm điểm hạng mục đổi mạnh.
**Chuyện gì xảy ra:** vi-iy tụt 0,26 vì một câu rơi khỏi top 5, vi-synonym tụt 0,167 vì vault chưa có lexicon. Người dùng chọn dùng gói vi cho bộ cài và yêu cầu thêm chế độ chi tiết V15b để điều tra từng hạng mục.
**Bài học:** Hạng mục có vài câu quá nhạy; đừng dùng cổng theo hạng mục cho bộ nhỏ, hoặc chỉ tính theo tổng.
**Artefact:** Bảng hạng mục trước và sau, không có câu hỏi.
