---
id: 2026-11-02-read-pkm-tu-doc-file-thay-3c6e
code: M-GYCY
aliases: [M-GYCY]
date: 2026-11-02
repo: repo
status: raw
signals: [khac, dao_quyet_dinh]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:2dfb5915#L3144", "claude:2dfb5915#L3170"]
hook: "OHS đang index 10 phút thì agent không đọc được note nào"
tension: chon_mot_mat_mot
sides: ["Chuyển việc đọc qua OHS như thiết kế ban đầu", "pkm tự đọc file để luôn dùng được, lệch khỏi plan"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# read: pkm tự đọc file thay vì chuyển qua OHS

**Bối cảnh:** Plan phase 17 ghi read chuyển tiếp sang OHS, nhưng hai agent đều phản đối.
**Chuyện gì xảy ra:** OHS chỉ đọc được note đã index, nên trong lúc khởi động hoặc index có thể mất khoảng 10 phút mà agent không đọc được note nào. Agent đề nghị pkm tự đọc file trong vault, luôn dùng được. Người dùng đồng ý, và plan lệch khỏi thiết kế ban đầu.
**Bài học:** Tool không cần index thì đừng để nó phụ thuộc vào index. Ghi rõ lệch khỏi plan khi người duyệt đổi quyết định.
