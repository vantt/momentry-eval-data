---
id: 2026-11-02-repo-private-artifact-cua-actions-bat-3c6e
code: M-3JCR
aliases: [M-3JCR]
date: 2026-11-02
repo: repo
status: raw
signals: [khac, dao_quyet_dinh]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1148", "claude:2dfb5915#L1162", "claude:2dfb5915#L1178", "claude:2dfb5915#L3804", "claude:2dfb5915#L3929"]
hook: "Repo public mà muốn tải artifact vẫn phải đăng nhập"
tension: tuong_ma_hoa_ra
sides: ["Fork public thì ai cũng tải được artifact", "GitHub bắt đăng nhập mới cho tải artifact Actions"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Repo private: artifact của Actions bắt đăng nhập, đến rc.3 đổi sang public

**Bối cảnh:** Bộ cài cần tải gói OHS từ artifact CI của fork, còn bản pkm thì nằm trong repo private.
**Chuyện gì xảy ra:** GitHub chỉ cho tải artifact của Actions khi đã đăng nhập, dù fork là public. Người dùng chọn giữ repo private, và bộ cài thử tải công khai trước rồi dự phòng bằng gh. Khi OHS có Release public, nguồn đổi sang Release. Đến rc.3 người dùng chuyển repo sang public, bộ cài không còn cần gh.
**Bài học:** Artifact CI và Release là hai nguồn tải khác nhau về quyền truy cập. Chọn nguồn phát hành theo quyền của người dùng cuối, không theo CI.
**Artefact:** Hai lệnh cài trước và sau khi public (không có tên người).
