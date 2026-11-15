---
id: 2026-11-02-ranh-gioi-fork-va-repo-du-40f9
code: M-0AB1
aliases: [M-0AB1]
date: 2026-11-02
repo: repo
status: raw
signals: [rang_buoc_thiet_ke, nguoi_duyet_may_soan]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L2238", "claude:c4caee3c#L2320", "claude:c4caee3c#L2372", "claude:c4caee3c#L2382", "claude:c4caee3c#L2411"]
hook: "Agent định làm hai việc trong fork, chúng thuộc repo khác"
tension: nguoi_dung_may_sai
sides: ["Agent đề xuất làm một phần trong lõi fork", "Người dùng hỏi từng mục và kết luận thuộc repo dự án"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Ranh giới fork và repo dự án: hai việc L13 và L22 không thuộc fork

**Bối cảnh:** PRD 9.0 quy định fork chỉ chứa cơ chế chung cho mọi người dùng OHS, không chứa logic sản phẩm.
**Chuyện gì xảy ra:** Agent ban đầu đề xuất làm một phần của hai việc gợi ý khi viết và sổ câu tìm trong lõi. Người dùng hỏi lại từng mục (plugin hay lõi, thuộc repo nào), rồi quyết định cả hai thuộc repo dự án. PRD mục 14.2 được cập nhật đúng như vậy.
**Bài học:** Quyết ranh giới repo trước khi viết mã. Hỏi 'thuộc repo nào' sớm để không đưa logic sản phẩm vào fork.
