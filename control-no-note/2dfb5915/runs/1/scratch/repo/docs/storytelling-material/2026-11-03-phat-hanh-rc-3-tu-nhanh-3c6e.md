---
id: 2026-11-03-phat-hanh-rc-3-tu-nhanh-3c6e
code: M-TJEG
aliases: [M-TJEG]
date: 2026-11-03
repo: repo
status: raw
signals: [dao_quyet_dinh, khac]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L3717", "claude:2dfb5915#L3881", "claude:2dfb5915#L3917", "claude:2dfb5915#L3954"]
hook: "Ra rc.3 từ nhánh chưa merge, main vẫn ở rc.2"
tension: khac
sides: ["Bản phát hành rc.3 đủ 7 file, checksum khớp", "Main vẫn ở rc.2, nhánh chờ một tuần chạy song song"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Phát hành rc.3 từ nhánh chưa merge, theo ý người duyệt

**Bối cảnh:** Plan ghi phase 17 chỉ merge vào main sau phase 16, tuần chạy song song.
**Chuyện gì xảy ra:** Người dùng yêu cầu ra rc.3 từ nhánh phase 17 để thử luôn. Agent tạo tag từ commit 535bc55, release có đủ 7 file và checksum khớp. Main vẫn ở rc.2, nhánh chờ merge sau tuần chạy song song.
**Bài học:** Khi người duyệt muốn thử sớm, phát hành thử từ nhánh riêng và ghi rõ ràng là chưa merge.
**Artefact:** Trang Release rc.3 (chụp, không lộ đường dẫn).
