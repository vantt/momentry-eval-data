---
id: 2026-10-09-fixture-phase-4-viet-tay-bay-4257
code: M-F00Q
aliases: [M-F00Q]
date: 2026-10-09
repo: repo
status: raw
signals: [khác]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L616", "omp:cd4449ab#L619", "omp:cd4449ab#L621", "omp:cd4449ab#L633", "omp:cd4449ab#L642", "omp:cd4449ab#L651", "omp:cd4449ab#L657", "omp:cd4449ab#L664", "omp:cd4449ab#L666"]
hook: "Fixture viết tay xanh ở lượt 7, rồi bị đòi thay bằng bản thật"
tension: tuong_ma_hoa_ra
sides: ["fixture tự viết đã xanh sau 7 lượt", "lead vẫn đòi thay bằng bản sao thật"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Fixture Phase 4 viết tay: bảy lượt sửa mới xanh

**Bối cảnh:** Fixture v1 ban đầu viết tay, chưa khớp layout thật nên các assert về trust và upstream đỏ.
**Chuyện gì xảy ra:** TestTrustVerdictAndUpstreamStatusUnchangedAfterMigration đỏ nhiều lần. Cần thêm thư mục approved, digest tài nguyên và meta đúng. Test xanh ở lượt thứ bảy. Lead sau đó yêu cầu thay bằng bản sao thật từ hub.
**Bài học:** Fixture viết tay dễ che lỗi. Đưa dữ liệu thật vào càng sớm càng tốt.
**Artefact:** Không cần.
