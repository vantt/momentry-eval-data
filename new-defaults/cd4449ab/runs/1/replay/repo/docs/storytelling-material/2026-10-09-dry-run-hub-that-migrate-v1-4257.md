---
id: 2026-10-09-dry-run-hub-that-migrate-v1-4257
code: M-Z62R
aliases: [M-Z62R]
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1462", "omp:cd4449ab#L1481", "omp:cd4449ab#L1484", "omp:cd4449ab#L1490", "omp:cd4449ab#L1702", "omp:cd4449ab#L1728", "omp:cd4449ab#L1731"]
hook: "Thử trên hub thật: file metadata bị coi là dữ liệu chính"
tension: tuong_ma_hoa_ra
sides: ["Tưởng .meta chỉ là metadata của hub", "Validator coi nó là entity chính và báo thiếu ID"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Dry-run hub thật: migrate v1→v2 chết vì .meta bị coi là entity canonical

**Bối cảnh:** Hub thật có skill v1 với thư mục .meta/ do hệ thống quản lý. Lead chạy thử migrate trên bản clone và thất bại ở bước v1→v2.
**Chuyện gì xảy ra:** Lỗi báo 'canonical entity is missing an ID' trên một file .meta/skill.yaml. Validator coi mọi file trong skill là entity canonical, kể cả .meta/ vốn chỉ là metadata hub. Fix: khi schema < 3, .meta/** bị loại khỏi validate canonical và chỉ đọc như input của Phase 0. Commit d348319 đổi 11 file, +340/-197 dòng.
**Bài học:** Trước khi viết validator, chạy thử trên một bản sao dữ liệu thật; fixture viết tay thường thiếu đúng những file mà dữ liệu thật có.
**Artefact:** Bảng số lỗi migrate trước và sau khi loại trừ .meta. Che tên skill và đường dẫn workspace.
