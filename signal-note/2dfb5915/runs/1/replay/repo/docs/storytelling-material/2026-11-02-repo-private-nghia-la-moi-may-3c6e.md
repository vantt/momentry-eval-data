---
id: 2026-11-02-repo-private-nghia-la-moi-may-3c6e
code: M-KMVS
aliases: [M-KMVS]
date: 2026-11-02
repo: repo
status: raw
signals: [rang_buoc_thiet_ke, dao_quyet_dinh]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1148", "claude:2dfb5915#L1160", "claude:2dfb5915#L1177", "claude:2dfb5915#L3804"]
hook: "Repo private nghĩa là khách nào cũng phải đăng nhập mới tải được"
tension: chon_mot_mat_mot
sides: ["Giữ repo private", "Khách không có gh không tải nổi OHS"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Repo private nghĩa là mọi máy khách phải gh login để cài, và quyết định giữ private rồi đổi sau

**Bối cảnh:** Bộ cài tải binary từ Release của repo chính, và repo này private. Phát hiện này xuất hiện khi kiểm tra lại đường tải OHS.
**Chuyện gì xảy ra:** Artifact của Actions yêu cầu đăng nhập ngay cả khi repo fork là public, nên khách không có gh không tải được OHS. Lúc đó repo chính còn private nên cả pkm cũng cần đăng nhập. Người dùng chọn giữ private, bộ cài có đường dự phòng bằng gh. Khi OHS có Release public, và repo sau đó đổi public, đường tải thẳng không cần đăng nhập nữa.
**Bài học:** Trước khi viết hướng dẫn cài, kiểm xem các đường tải có cần đăng nhập không; quyền truy cập của repo quyết định cả trải nghiệm cài.
**Artefact:** Đoạn so sánh ba cách phát hành (public, private, repo Release riêng).
